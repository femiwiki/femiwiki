# How to contribute to extensions

## Branches

The [compatibility policy] of FemiWiki extensions/skin is "release branches", that means for every MediaWiki release, there is a corresponding branch in the extension.
`master` branch is the default branch where the commits pushed. But the commits on master are strongly recommended to backported in latest stable MW release(`REL1_XX`) branch which is deployed by FemiWiki website.

## Release

1. Checkout the latest stable MediaWiki release branch (not master): `git checkout REL1_XX && git pull`.
2. Update the CHANGELOG.md
3. Edit "version" of extension.json or skin.json
4. ```sh
    NAME=OurExtension
    # NAME=$(basename $(pwd))
    VERSION=vx.x.x
    # Commit the changes.
    git commit -m "Release ${VERSION}"
    # Tag the commit with message
    git tag "${VERSION}" -m "${NAME} release"
    # Push the commit and the tag
    git push --follow-tags
   ```
5. (optional) Copy changelog from the file to the release page.

Then PR for that release to [docker-mediawiki repository] will be created automaticlly.

[docker-mediawiki repository]: https://github.com/femiwiki/docker-mediawiki
[compatibility policy]: https://www.mediawiki.org/wiki/Compatibility#mediawiki_extensions
