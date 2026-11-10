# docs-is

> **On the new cloud line (`docs-v2-cloud`, staging only):** this repo holds only `asgardeo/`, the Older cloud Doc space Asgardeo (the old Cloud, frozen). Identity & Access Management, with its new Cloud, is in the private `identity-platform-cloud` repo on that line, until Editions can name their repo.

A Content repo of WSO2 Docs. It holds one Doc space, `identity-and-access-management/` (Identity & Access Management):

| Edition | What | Branch |
|---|---|---|
| Cloud, "Identity & Access Management" | today's https://wso2.com/identity-platform/docs/ (formerly Asgardeo) | `docs-v2/main` |
| Self-hosted, "Identity Server <version>" | Identity Server 7.3.0, 7.2.0, 7.1.0, 7.0.0 | `docs-v2/main`, folder `identity-and-access-management/<version>/` |
| `next` (preview only) | the unreleased Identity Server | `docs-v2/main` |

Older versions are not on WSO2 Docs (`legacyVersions` in `docspace.yaml`): Identity Server 6.1.0, 6.0.0, 5.11.0, 5.10.0 and 5.9.0 stay on https://is.docs.wso2.com, and 5.0.0 to 5.8.0 on their Confluence docs.

Until the cutover, `master` is still the legacy MkDocs sites (`en/`), which build wso2.com/identity-platform/docs/ and is.docs.wso2.com, and writers still merge there. Every branch of the WSO2 Docs layout starts with `docs-v2/`. Until then the pages on these branches are generated from `master` by the rebuild (`tools/rebuild/rebuild.mjs convert identity-management` in the onboarding workspace, with `tools/onboard-mkdocs/convert-identity.mjs`): don't edit them here, the next run overwrites them. At the cutover the branches drop `docs-v2/` and `docs-v2/main` becomes the main line.

Docs releases are tagged `identity-and-access-management/cloud-<YYYY.MM.DD>.<n>` (Cloud, from the main line) and `identity-and-access-management/<version>-docs.<n>` (a version, from its folder on the main line).

`identity-and-access-management/` holds `docspace.yaml` (the Doc space manifest), `editions.yaml` (per-Edition variables such as the product name), `redirects.yaml` (page moves), `docs/` (pages; folders are the sidebar) and `assets/` (images and files its pages use). Where Cloud and Identity Server differ, pages carry Edition markers (`editions:`, `selfHostedFrom:`, `<Edition only="…">`).

The tools are on GitHub Packages. Once per machine, make a classic personal access token with `read:packages` (authorised for the `wso2-enterprise` organisation's SSO if it asks), then run `npm login --scope=@wso2-enterprise --auth-type=legacy --registry=https://npm.pkg.github.com` with your GitHub user name and the token as the password. This repo's `.npmrc` names the registry for `@wso2-enterprise`; it holds no token.

Get started, from setting up your computer to a Docs release going live: the WSO2 Docs Platform's README, https://github.com/wso2-enterprise/choreolabs-docs#readme.

Licensed under the Apache License 2.0 (`LICENSE`).
