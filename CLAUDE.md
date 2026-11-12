@AGENTS.md

## This repo

- One Doc space, Identity Management (`identity-management/`). Cloud and the unreleased `next` are built from `docs-v2/main`, one tree with Edition markers where they differ; each released Identity Server version is `docs-v2/identity-management/release/<version>`.
- A whole folder shown in one Edition only says so in its `_category_.yml` (`customProps: { editions: cloud }`). A page whose sidebar folder differs from its old address keeps that address with `slug:`.
- The text names the product through `{edition.productName}`: "WSO2 Identity Platform" on Cloud, "WSO2 Identity Server" on a version.
- Until the cutover the pages here are generated from `master` (MkDocs, `en/`) by the onboarding workspace's `tools/onboard-mkdocs/convert-identity.mjs`: fix the source on `master` or the script's rules, not the pages here.
