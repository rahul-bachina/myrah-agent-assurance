# Product strategy

## Market conclusion

Myrah Agent Assurance is not the first AI-agent security product. Microsoft, major security vendors, specialist AI-security companies, and open-source projects already cover parts of agent discovery, runtime protection, MCP inspection, red teaming, and governance.

The opportunity is a focused product gap:

> An affordable, local-first assurance workbench for Microsoft-centric organisations that spans Copilot Studio, GitHub Copilot harness projects, skills, MCP, exported solutions, and UK governance evidence without requiring a complete premium security stack.

## Microsoft overlap

Microsoft currently provides substantial capabilities:

- Power Platform inventory discovers agents, apps, flows, environments, and connector usage.
- Copilot Agent Kit reviews Copilot Studio and Microsoft 365 declarative agents.
- Defender discovers many local agents and some MCP configurations.
- Defender for Cloud provides AI security posture for supported cloud agents.
- Purview provides data-security posture and AI interaction visibility where licensed.
- Project Perception describes an emerging continuous containment architecture.

Therefore this project must complement Microsoft instead of copying a Microsoft dashboard.

## Defensible wedge

1. Offline and local-first assessment.
2. GitHub Copilot harness, `SKILL.md`, exported solution, and MCP coverage in one evidence model.
3. Transparent rules without mandatory AI or Copilot-credit consumption.
4. UK public-sector and regulated-industry assurance mappings.
5. Affordable organisation-based licensing.
6. Pre-deployment scanning and CI evidence.
7. Clear integration paths for customers who already own Microsoft security products.

## Open-core model

### Community — MIT

- offline scanner;
- base rules;
- JSON, SARIF, and HTML;
- local configuration comparison;
- vulnerable fixtures and extension contracts.

### Professional — commercial

- tenant-connected inventory;
- exposure graph;
- encrypted history and change detection;
- enhanced UK profiles and reports;
- active synthetic tests;
- integrations and supported builds.

Commercial code will live separately. The MIT repository will not contain disabled paid features hidden behind a licence key.

## Pricing hypothesis

Pricing must be tested with design partners before publication as a promise.

| Edition | Indicative annual price | Scope |
|---|---:|---|
| Community | £0 | Offline scanning and base reports |
| Professional | £299 | One tenant, unlimited internal users and agents |
| Organisation | £799 | Up to five tenants, policy packs and CI gates |
| MSP | £1,999 | Up to 25 customer tenants and multi-tenant reporting |

## First demonstrator

Use a fictional agent containing:

- anonymous access;
- an unrestricted HTTP tool;
- a synthetic exposed secret;
- a consequential action without approval;
- an instruction that trusts retrieved website content.

The scanner should identify all five conditions without executing the agent and produce a local evidence report. A corrected configuration should pass those same checks.

## Evidence sources

- [Microsoft: Securing the agentic insider](https://blogs.microsoft.com/blog/2026/10/19/securing-the-agentic-insider/)
- [Defender AI agent support matrix](https://learn.microsoft.com/en-us/defender-endpoint/ai-agent-support-matrix)
- [Power Platform inventory](https://learn.microsoft.com/en-us/power-platform/admin/power-platform-inventory)
- [Copilot Agent Kit review tool](https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/kit-agent-review-tool)
- [Microsoft open-source Agent Governance Toolkit](https://opensource.microsoft.com/blog/2026/04/02/introducing-the-agent-governance-toolkit-open-source-runtime-security-for-ai-agents/)

## Decision gate

Proceed beyond feasibility only if the spike proves that we can provide at least five high-confidence findings that are not already presented clearly by the standard Microsoft maker and administrator experiences.
