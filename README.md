# Big Orange Lab Plugins

A monorepo of WordPress.org plugins for Big Orange Lab.

<!-- deploy-status-start -->
<!-- deploy-status-end -->

## Plugins

| Plugin                                          | GitHub                                                                                      | Description                             |
| ----------------------------------------------- | ------------------------------------------------------------------------------------------- | --------------------------------------- |
| [bol-split-testing](bol-split-testing/)         | [bigorangelab/bol-split-testing](https://github.com/bigorangelab/bol-split-testing)         | A/B Split Testing for WordPress.        |
| [bol-easy-translations](bol-easy-translations/) | [bigorangelab/bol-easy-translations](https://github.com/bigorangelab/bol-easy-translations) | Easy string translations for WordPress. |
| [big-orange-pardot](big-orange-pardot/)         | [bigorangelab/big-orange-pardot](https://github.com/bigorangelab/big-orange-pardot)         | Pardot integration for WordPress.       |

## Repo structure

```
<plugin-slug>/          ← plugin source (git submodule)
.github/workflows/      ← deploy.yml, asset-update.yml, version-check.yml for WordPress.org publishing
```

Plugins are tracked as git submodules, each with their own commit history and default branch.

## Deploying to WordPress.org

Releases are published via the `.github/workflows/deploy.yml` workflow (manually triggered). It bumps versions, syncs to SVN, opens a version-bump PR back against the plugin's default branch, and updates the deploy-status table at the top of this README.

See [ACTIONS.md](ACTIONS.md) for full workflow documentation, required credentials, and the version-tracking system.

## Working with this repo

See [AGENTS.md](AGENTS.md) for coding conventions, build tooling, and linting guidance.
