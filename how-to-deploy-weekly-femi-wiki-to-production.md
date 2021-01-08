# How to Deploy Weekly FemiWiki to Production

## Docker Swarm

1. Review the changes of each extension or skin since their latest releases.

   ```sh
   # Use this script to get URLs of comparison pages (python required)
   BRANCH=REL1_35
   EXTENSIONS="AchievementBadges FacetedCategory Sanctions UnifiedExtensionForFemiwiki FemiwikiSkin"
   for EXT in $EXTENSIONS; do
     LATEST=$(curl -sL https://api.github.com/repos/femiwiki/"${EXT}"/releases/latest | python -c 'import json,sys;print(json.loads(sys.stdin.read())["tag_name"])')
     echo https://github.com/femiwiki/${EXT}/compare/"${LATEST}".."${BRANCH}"; done
   ```

2. Release all extensions that has changes. Read [how-to-contribute-to-extensions.md#release] for details.
3. Bump the extensions on [femiwiki/docker-mediawiki] repository. ([commit example](https://github.com/femiwiki/docker-mediawiki/commit/01ff89a7))
4. Wait for a new docker image to be built. You can see the progress of the building process in the [Github workflow page].
5. After building, copy a new latest docker image's tag from the [Github packages page].
6. Edit [production.yml] file and commit. ([commit example](https://github.com/femiwiki/docker-mediawiki/commit/68994922))
7. Make sure that our database backup is stored well.
8. Connect our AWS EC2 instance.
9. Execute:

   ```sh
   # Go to owr mediawiki clone directory
   cd mediawiki
   # Checkout the latest master branch.
   git checkout master && git pull

   # If needed
   # docker stack rm mediawiki

   # Deploy the new compose file
   docker stack deploy -c production.yml --prune mediawiki
   # Prune docker system
   # See https://github.com/femiwiki/femiwiki/issues/70#issuecomment-482030123
   docker system prune -fa --volumes
   # See status
   # watch docker service ls
   ```
10. Update [CHANGELOG.md].

## Nomad

TBD. FemiWiki is not deployed by Nomad yet. (https://github.com/femiwiki/femiwiki/issues/116)

[how-to-contribute-to-extensions.md#release]: https://github.com/femiwiki/femiwiki/blob/main/how-to-contribute-to-extensions.md#release
[femiwiki/docker-mediawiki]: https://github.com/femiwiki/docker-mediawiki
[github workflow page]: https://github.com/femiwiki/docker-mediawiki/actions
[github packages page]: https://github.com/orgs/femiwiki/packages/container/package/mediawiki
[production.yml]: https://github.com/femiwiki/docker-mediawiki/blob/master/production.yml
[changelog.md]: https://github.com/femiwiki/femiwiki/blob/main/CHANGELOG.md
