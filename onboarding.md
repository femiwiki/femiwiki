# Onboarding

A checklist for people joining the dev team to work on the frontend: the skin
and the gadgets. Backend and infrastructure access (AWS, OpenTofu) is out of
scope here.

## Accounts

- [ ] A [femiwiki.com] account
- [ ] Membership in the [femiwiki GitHub organization]

## Read first

- [ ] [coding-conventions.md](coding-conventions.md)
- [ ] [how-to-contribute-to-extensions.md](how-to-contribute-to-extensions.md)
- [ ] The [frontend contribution guide] slides (Korean)

## Skin

- [ ] Clone [femiwiki/FemiwikiSkin]
- [ ] Run a local wiki with the skin: `npm i && npm run dev`. It downloads
      MediaWiki and a web server (about 500 MB) and needs internet access. The
      wiki listens on <http://localhost:2019>; log in as `Admin` with password
      `Adminpassword`.
- [ ] Run `npm test` before pushing
- [ ] Open a first PR

## Gadgets

- [ ] Clone [femiwiki/remote-gadgets]. Each file under `gadgets/`, `pages/` and
      `lua/` is one wiki page, named after the page title in URL encoding (for
      example `gadgets/bookflap/mediawiki%3Agadget-bookflap.js` is
      `MediaWiki:Gadget-bookflap.js`).
- [ ] Understand deployment: a push to `main` runs `apply.py` in GitHub
      Actions, which saves the files changed since the last run to their wiki
      pages as the gadget bot. Change those pages here, not on the wiki: the
      next change to a file overwrites its page.

[femiwiki.com]: https://femiwiki.com
[femiwiki GitHub organization]: https://github.com/femiwiki
[frontend contribution guide]: ko/프론트엔드%20기여%20가이드.md
[femiwiki/FemiwikiSkin]: https://github.com/femiwiki/FemiwikiSkin
[femiwiki/remote-gadgets]: https://github.com/femiwiki/remote-gadgets
