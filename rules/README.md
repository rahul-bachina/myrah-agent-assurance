# Rules

This directory will contain versioned deterministic Community rules.

Each rule must define:

- stable ID and version;
- title, category, severity, and supported formats;
- exact evidence requirements;
- detection and non-detection examples;
- remediation;
- authoritative references;
- limitations and expected false-positive conditions.

Missing or inaccessible evidence must produce `not_evaluated` or `insufficient_evidence`, never `pass`.
