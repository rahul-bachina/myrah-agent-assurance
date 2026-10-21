# Security policy

## No production release yet

The repository is currently a product foundation and does not contain a supported production scanner. Security guarantees must not be inferred from this repository or its outputs.

## Reporting a vulnerability

Please do not publish an exploitable vulnerability before coordinated review. Email **info@myrah.co.uk** with:

- affected file, component, or release;
- reproduction steps using synthetic data;
- likely impact;
- suggested mitigation, if known.

Do not include customer information, live credentials, access tokens, or confidential agent configurations.

## Intended security properties

The scanner will:

- treat all scanned files and metadata as untrusted;
- avoid executing discovered commands, MCP servers, plug-ins, or tools;
- apply archive traversal, decompression, file-count, size, and duration limits;
- sanitize report content and prevent external asset loading;
- redact secrets from logs and reports where possible;
- use delegated read permissions before requesting broader access;
- keep offline scans offline;
- state evidence limitations beside every result.

These are design goals until verified by tests and a published release.
