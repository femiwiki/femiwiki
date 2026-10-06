# How to Deploy Weekly FemiWiki to Production

1. Merge the change into the `main` of FemiwikiSkin or UnifiedExtensionForFemiwiki.
   A bot opens a pull request on [femiwiki/docker-mediawiki] that pins the new
   commit, and the image bumps that follow merge on their own once green. The
   other extensions follow the branches in `extensions.json` and are bumped by
   a monthly workflow on [femiwiki/docker-mediawiki].
2. Wait for the image build. The [Github workflow page] shows it, and when it
   finishes a pull request bumping the image tag opens on [femiwiki/infra] by
   itself. Nothing needs copying by hand.
3. **Decide whether this release carries a schema change**, and if it does, read
   [Releases that change the schema](#releases-that-change-the-schema) below
   before going on. A release that needs `update.php` is not a zero-downtime
   release.
4. Make sure the database backup is stored well.
5. Approve the `docker` environment on the bump pull request's run under
   [infra Actions]. **The approval is what applies to production, not the
   merge.** It is offered only once the pull request's required checks pass
   and it has no conflict. A branch behind `main` may still be applied: the
   apply makes a fresh plan and refuses if `main` changed the same workspace,
   in which case merge `main` into the branch and approve the new run.
6. Watch the apply. On success it re-plans on the same runner, fails if
   anything is left over, and merges the pull request itself.
7. Check that the wiki is up, and that the container generation moved:

   ```sh
   curl -o /dev/null -w '%{http_code} %{time_total}s\n' https://femiwiki.com/w/페미위키:대문
   ```

## Releases that change the schema

`MEDIAWIKI_SKIP_UPDATE=1` is set on the `fastcgi` container, so nothing runs
`update.php` on its own. It is a deliberate, one-shot step against the shared
database, and it is the step that makes a release not zero-downtime.

A deploy starts the new `fastcgi` container beside the old one and drains the
old one only once the new one is healthy, so **for the length of that overlap
two different images are talking to the same MySQL**. That is what shapes the
rules:

- **Additive first.** New columns, tables and indexes, and dual-write migration
  stages, can be applied while both images run: the old code ignores what it
  does not know about. Run `update.php` before the apply.
- **Destructive last, and never during the overlap.** Drops, renames and
  read-new-only stages break the draining old container. They wait for a
  release after the one that stopped reading the old shape.
- **Never roll back across a destructive step.** Reverting the image is safe
  only while the schema is still readable by the older code.
- **Say which it is.** Note in the pull request whether the release carries a
  schema change and which half it is.

When a change genuinely cannot be made additive, take the read-only window
rather than pretending the deploy is safe. The line is in
`infra/serving/Hotfix.php`, commented out; since that file is passed to the
container from `infra`, turning it on and off again is a `tofu apply` each way.
Announce it on `미디어위키:Sitenotice`.

## If it goes wrong

The bump pull request only changes the image tag and the generation, so
reverting is applying the previous tag. The prior image stays in ghcr.

An apply that fails leaves production alone: the replacement container is
created before the old one is destroyed, so a container that never becomes
healthy means a failed apply and the old one still serving.

**Do not leave an applied pull request unmerged.** Until it lands, `main`
describes less than what is deployed, and an apply from any other branch plans
against `main` and takes production back. The apply merges its own pull request
for this reason; if that ever fails, merge it by hand before applying anything
else.

[femiwiki/docker-mediawiki]: https://github.com/femiwiki/docker-mediawiki
[femiwiki/infra]: https://github.com/femiwiki/infra/pulls
[github workflow page]: https://github.com/femiwiki/docker-mediawiki/actions
[infra actions]: https://github.com/femiwiki/infra/actions/workflows/tofu.yml
