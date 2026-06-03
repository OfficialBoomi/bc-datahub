# bc-datahub

Notes for developers working on this plugin.

## What's here

A Boomi Companion plugin shipping the `boomi-datahub` skill for Boomi DataHub (master data management). See `README.md` for user-facing setup (the `.env` and `.claude/settings.json` contract) and `skills/boomi-datahub/` for the skill itself.

`bc-datahub` plugin is standalone-installable. If `bc-integration` plugin or `boomi-integration` skill is already setup in the same workspace, some Platform details are re-used by this skill/plugin; otherwise they should be set directly in `.env`.

## Architecture

DataHub's APIs don't share path prefixes with the Boomi Platform REST API that `bc-integration` covers (`/mdm/api/rest/v1` vs `/api/rest/v1`). The per-skill helper `skills/boomi-datahub/scripts/datahub-common.sh` provides DataHub-specific URL builders and the shared API wrapper.

