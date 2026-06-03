# Changelog

## 0.1.1

- `datahub-env-check.sh` now validates repository API .env vars when `DATAHUB_REPO_*` are set; warns non-fatally on failure. (Previously only validated platform credentials)
- Refined `boomi-datahub` scope to currently shipped capability.

## 0.1.0

- Minor bump: first published release of bc-datahub.
- First pass at `bc-datahub` — a new bc-* plugin shipping the `boomi-datahub` skill for Boomi DataHub (MDM) configuration and operations. Covers model / source / repository / deployment / quarantine / golden-record verbs via sub-commanded bash scripts, with Platform API and Repository API auth sourced from `.env`. Golden-record operations gated behind `ALLOW_GR_ACTIONS=true`.
