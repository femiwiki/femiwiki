# How to Deploy Weekly FemiWiki to Production

1. Review the changes of each extension or skin since their latest releases.

   ```sh
   # Use this script to get URLs of comparison pages (python required)
   BRANCH=REL1_43
   EXTENSIONS='
     AchievementBadges
     DiscordRCFeed
     FacetedCategory
     FemiwikiSkin
     PageViewInfoGA
     Sanctions
     UnifiedExtensionForFemiwiki
   '
   for EXT in $EXTENSIONS; do
     LATEST=$(curl -sL https://api.github.com/repos/femiwiki/"${EXT}"/releases/latest | python -c 'import json,sys;print(json.loads(sys.stdin.read())["tag_name"])')
     echo https://github.com/femiwiki/${EXT}/compare/"${LATEST}".."${BRANCH}"; done
   ```

2. Release all extensions that has changes. Read [how-to-contribute-to-extensions.md#release] for details.
3. Bump the extensions on [femiwiki/docker-mediawiki] repository.
4. Wait for a new docker image to be built. You can see the progress of the building process in the [Github workflow page].
5. After building, copy the new `femiwiki` image tag from the [Github packages page].
6. Bump the `femiwiki` image tag (the `fastcgi` and `http` containers) in [infra/docker/container.tf] and commit.
7. Wait that the Terraform run planned.
8. Make sure that our database backup is stored well.
9. Confirm the terraform apply.

[how-to-contribute-to-extensions.md#release]: https://github.com/femiwiki/femiwiki/blob/main/how-to-contribute-to-extensions.md#release
[femiwiki/docker-mediawiki]: https://github.com/femiwiki/docker-mediawiki
[github workflow page]: https://github.com/femiwiki/docker-mediawiki/actions
[github packages page]: https://github.com/orgs/femiwiki/packages/container/package/femiwiki
[infra/docker/container.tf]: https://github.com/femiwiki/infra/blob/main/docker/container.tf
