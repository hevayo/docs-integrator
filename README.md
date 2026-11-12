# docs-integrator

A Content repo of WSO2 Docs (docs.wso2.com). On the `docs-v2/` branches it holds these Doc spaces:

| Directory | Doc space | Editions and branches |
|---|---|---|
| `integration/` | Integration: the Integration Platform on WSO2 Cloud, the family-level Doc space of the Integration family | Cloud on `docs-v2/main` |
| `integrator/` | WSO2 Integrator: a Sub Doc space of `integration` | Self-hosted versions on `docs-v2/integrator/release/<version>` (5.1.0); `docs-v2/main` holds the next version |

WSO2 Agent Builder (a Sub Doc space of `integration`, release branches `docs-v2/agent-builder/release/<version>`) and WSO2 Connectors follow. Docs releases are tagged `integration/cloud-<YYYY.MM.DD>.<n>` and `integrator/<version>-docs.<n>`; tags carry no `docs-v2/`.

Until the cutover, `main`, `saas`, `wso2-integrator`, `wso2-agent-builder` and `wso2-connectors` are still the legacy Docusaurus sites and their deploy pipelines, and writers still merge there. `docs-v2/main` is the WSO2 Docs main line, cut from `main`. Its pages are converted from the product branches (`integration/` from `saas`, `integrator/` from `wso2-integrator`) by the onboarding tools, not merged: don't edit them by hand until the cutover. At the cutover a PR merges `docs-v2/main` into `main` and the `docs-v2/` prefix goes.

Each Doc space directory holds `docspace.yaml` (the Doc space manifest), `editions.yaml` (per-Edition variables), `redirects.yaml` (page moves), `docs/` (pages; folders are the menu), `partials/` and `assets/` (images).

The repo root holds only shared files: this README, `CODEOWNERS`, the release workflow (`.github/workflows/docs-bundle-release.yml`; it releases from `docs-v2/main` and the `docs-v2/` release branches), the branch ruleset (`.github/branch-ruleset.json`), the editor settings, the writing style guide (`.github/instructions/`), the issue and pull request templates, and `AGENTS.md` and `CLAUDE.md` for agents (they point to `npx @wso2-enterprise/docs help`). The Platform-managed files come from `templates/content-repo/` in `wso2-enterprise/choreolabs-docs`.

The tools are on GitHub Packages. Once per machine, make a classic personal access token with `read:packages` (authorised for the `wso2-enterprise` organisation's SSO if it asks), then run `npm login --scope=@wso2-enterprise --auth-type=legacy --registry=https://npm.pkg.github.com` with your GitHub user name and the token as the password. This repo's `.npmrc` names the registry for `@wso2-enterprise`; it holds no token.

Get started, from setting up your computer to a Docs release going live: the WSO2 Docs Platform's README, https://github.com/wso2-enterprise/choreolabs-docs#readme.
