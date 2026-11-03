# Agent operating instructions

<!-- weavestream-records:start -->
## Weavestream records and credentials

Weavestream is the system of record for operational information, applications and
credentials: [TegridyHosting assets](https://weavestream.tegridyhosting.com/admin/companies/d4bd8eb5-0bf8-4eb7-b453-4491e80a1844/assets).
Company ID: `d4bd8eb5-0bf8-4eb7-b453-4491e80a1844`.

- Store passwords, tokens, private keys, recovery codes and TOTP secrets in the
  **Weavestream vault**, linked to the relevant asset. Use unique credentials per
  service/identity. Keep values out of git, logs, chat, documents and ordinary
  flexible-asset fields. Never truncate a secret; use an encrypted vault note for
  material exceeding the password field's limit. Deployment secret stores and
  ignored workstation files are delivery/cache locations, not the system of record.
- Store applications, services, repositories, hosts, environments and dependencies
  as **flexible assets** with structured fields and relationships. Record ownership,
  purpose, estate/environment, current state, endpoints, source repository,
  deployment/Semaphore references, backup/recovery references and credential links.
  Reuse existing records; retain confirmed retirement/disabled states.
- Store high-level architecture, decisions, operating procedures and recovery
  guidance as **Documents**, linked to the relevant flexible assets and source
  files. Keep content concise and specific: explain purpose, dependencies, how to
  operate/verify/recover, and where the authoritative implementation lives.
- Update affected assets, vault references and Documents **in the same change**
  whenever configuration, ownership, access, deployment or recovery behaviour
  changes. Record an actual UTC verification time and evidence (commit, task or
  observed result). Verify writes by reading them back. A task is incomplete until
  these records match its verified result; report an access failure rather than
  silently leaving stale information or inventing a successful verification.
- Read Weavestream before asking for credentials or recreating documentation.
  Use its authenticated API or approved OAuth/MCP connection. Preserve scoped
  permissions and secret-reveal restrictions; do not expose credentials to agents
  or integrations that cannot retrieve them. Hudu is a legacy migration source,
  not a destination for new or updated records. Keep historical integration names
  and compatibility variable names intact until their implementations are migrated.

Git remains authoritative for executable code and deployment intent. Weavestream
holds the current operational record and links to the relevant revision.
<!-- weavestream-records:end -->
