@AGENTS.md

## This repo

- One Doc space, Identity & Access Management (`identity-and-access-management/`). Cloud and the unreleased `next` are built from `docs-v2/main`, one tree with Edition markers where they differ; each released Identity Server version is a folder on the same branch, `identity-and-access-management/<version>/` (its own `docs/`, `assets/` and `redirects.yaml`).
- A whole folder shown in one Edition only says so in its `_category_.yml` (`customProps: { editions: cloud }`). A page whose sidebar folder differs from its old address keeps that address with `slug:`.
- The text names the product through `{edition.productName}`: "WSO2 Identity Platform" on Cloud, "WSO2 Identity Server" on a version.
- Until the cutover the pages here are generated from `master` (MkDocs, `en/`) by the onboarding workspace's rebuild (`tools/rebuild/identity-management/`, the recipe, and `tools/onboard-mkdocs/convert-identity.mjs`): fix the source on `master`, the recipe or the script's rules, not the pages here.
