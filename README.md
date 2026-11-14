# CIPP-API

SentraCX's fork of the PowerShell/Azure Functions backend for CIPP's Microsoft 365 administration interface. The companion frontend is [sentraCX/CIPP](https://github.com/sentraCX/CIPP).

## Source and documentation

| Path | Purpose |
| --- | --- |
| [host.json](host.json), [profile.ps1](profile.ps1) | Functions host settings and startup |
| [Modules/](Modules/) | Bundled PowerShell modules, including API implementations and tests |
| [Modules/CIPPTests/](Modules/CIPPTests/) | Per-test reference pages; identifiers are distinct even where wording is shared |
| [Config/openapi.json](Config/openapi.json) | Base API schema |
| [.build/README.md](.build/README.md) | OpenAPI enrichment, frontend extraction and schema validation |
| [AGENTS.md](AGENTS.md) | Owner execution policy and credential/operational-record rules |
| [license.md](license.md) | Upstream licensing |

Modules are bundled in `Modules/` and loaded explicitly; [requirements.psd1](requirements.psd1) is intentionally empty. Keep Functions settings and tenant credentials in the approved secret delivery environment, outside source.

The build guide records the enrichment commands and their pinned lint baseline. Retained workflow definitions describe upstream build/release machinery; the owner policy in `AGENTS.md` governs execution for this fork. Source cleanup does not enable workflows, deploy Functions or contact customer tenants.
