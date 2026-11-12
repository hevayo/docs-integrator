@AGENTS.md

## This repo

- `integration/` (Integration, Cloud only) and its Sub Doc space `integrator/` (WSO2 Integrator; its versions on `docs-v2/integrator/release/<version>`, the next version on `docs-v2/main`). WSO2 Agent Builder will be another Sub Doc space, and WSO2 Connectors a Doc space of its own, in this repo.
- Until the cutover, the legacy product branches (`saas`, `wso2-integrator`, `wso2-agent-builder`, `wso2-connectors`) are the Docusaurus sites and writers merge there. `integration/` is converted from `saas` and `integrator/` from `wso2-integrator` by the onboarding tools; don't hand-edit them, or the next conversion overwrites the change.
- The pages say "WSO2 Integrator" and "WSO2 Cloud", the product's names. "Integration" is the Doc space's and the family's name on WSO2 Docs.
- Links to WSO2 Integrator pages go to its live docs (`https://wso2.com/integration-platform/docs/integrator/…`) until it is on WSO2 Docs; then they become `docs:integrator/…` links.
