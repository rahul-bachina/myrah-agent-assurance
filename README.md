# Myrah Agent Assurance

Local-first security and governance assessment for AI agents.

> See every agent. Understand every connection. Keep people in control.

## Status

This repository contains the **Community concept and foundation** for Myrah Agent Assurance. It is an early-stage, MIT-licensed project: the initial rule catalogue and scanner implementation are being designed in public.

Do not use the current repository as a security guarantee or compliance certification.

## The problem

AI agents combine models, instructions, identities, knowledge, tools, connectors, MCP servers, and execution environments. A configuration that looks harmless in isolation can create a risky data or action path when those components are connected.

Organisations need practical answers:

- Which agents exist and who owns them?
- What can each agent read, write, send, publish, or delete?
- Which connectors, tools, skills, and MCP servers can it use?
- Where is meaningful human approval required?
- What changed since the previous assessment?
- What evidence supports each security conclusion?

## Community vision

The Community edition will scan agent projects and exported configurations without executing their tools. Planned targets include:

- Microsoft Copilot Studio solution exports;
- GitHub Copilot harness projects;
- agent instructions and reusable `SKILL.md` files;
- MCP server manifests and tool declarations;
- evaluation suites and deployment configuration;
- Microsoft 365 declarative agent packages.

Planned outputs:

- evidence-backed findings with severity and confidence;
- JSON for automation;
- SARIF for code-security workflows;
- self-contained HTML reports;
- configuration comparison between two versions.

## Product boundary

The open-source scanner is intended to remain genuinely useful. A separate affordable Professional product is planned for live tenant inventory, exposure graphs, encrypted assessment history, change monitoring, enhanced UK policy packs, integrations, and team workflows.

Myrah Agent Assurance is designed to complement Microsoft Defender, Purview, Sentinel, Agent 365, Power Platform governance, and the Copilot Agent Kit. It is not a replacement for endpoint protection, enterprise DLP, a SOC, or formal penetration testing.

## Design principles

1. Read-only by default.
2. Deterministic checks before optional AI analysis.
3. Treat scanned content as untrusted data, never as instructions.
4. Never execute discovered MCP servers, scripts, or agent tools.
5. Missing evidence is not a pass.
6. Every finding includes evidence, limitations, and remediation.
7. Human approval before consequential tests or changes.
8. Offline operation without mandatory telemetry.
9. Transparent versioned rules.
10. No claim that a clean scan means an agent is secure.

## Proposed assessment domains

| Domain | Examples |
|---|---|
| Identity and ownership | Missing owner, anonymous use, unsuitable shared identity |
| Data and knowledge | Excessive visibility, unsafe data paths, exposed secrets |
| Tools and MCP | Dangerous writes, unrestricted HTTP, mutable MCP packages |
| Human control | Missing approval, escalation, refusal, or evidence rules |
| Deployment governance | Default environment, unmanaged release, stale review |
| Testing and operations | No injection tests, audit evidence, incident owner, or stop procedure |

## Roadmap

See [ROADMAP.md](ROADMAP.md) for delivery milestones and [docs/PRODUCT-STRATEGY.md](docs/PRODUCT-STRATEGY.md) for the open-core product model.

The first demonstrator will scan a deliberately vulnerable fictional agent, surface five evidence-backed findings, and generate a local HTML report.

## Security

This project will process potentially hostile configurations. Read [SECURITY.md](SECURITY.md) before reporting a vulnerability. The threat model and parser limits will be published before the first executable release.

## Contributing

The project is not yet accepting large code contributions while the canonical model and extension interfaces are being defined. Research, rule proposals, fixtures, and reproducible security findings are welcome through GitHub issues. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Professional services

Myrah helps UK public and private sector organisations design, build, test, and govern AI agents across Microsoft, Azure, AWS, and Google Cloud.

For an agent security review or implementation engagement, contact **info@myrah.co.uk** or visit [myrah.co.uk](https://myrah.co.uk).

## Licence

Community source code and original documentation in this repository are licensed under the [MIT License](LICENSE), unless a file says otherwise. Microsoft and other product names are trademarks of their respective owners. This project is independent and is not endorsed by Microsoft.
