# Architecture direction

## Proposed stack

- .NET 10 and C# for the canonical model, adapters, rule engine, and CLI.
- Avalonia UI for a signed Windows-first desktop application with cross-platform potential.
- MSAL.NET for delegated Microsoft Entra authentication.
- SQLite for local evidence, with sensitive fields encrypted using an OS-protected key.
- JSON and SARIF as canonical machine-readable outputs.
- Self-contained sanitized HTML as the first human-readable report.

## Logical flow

```text
Source adapter
  -> canonical agent graph
  -> deterministic policy engine
  -> findings with evidence and confidence
  -> JSON / SARIF / HTML
```

Planned source adapters:

- local folder or Git repository;
- exported solution ZIP;
- Power Platform Inventory API;
- Azure Resource Graph;
- optional Dataverse, Microsoft Graph, Defender, Sentinel, and Purview enrichment.

## Trust boundary

Parsed agent content is hostile input. It must not be placed into an execution context, shell command, active MCP session, unsanitized HTML report, or privileged model instruction.

## Permission strategy

- offline scan requires no identity or network access;
- tenant discovery uses delegated user authentication;
- request the narrow AI Reader role where it provides sufficient inventory;
- separate optional enrichment permissions from the default connection;
- no tenant writes in Community or the first Professional release.
