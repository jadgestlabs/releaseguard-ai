# ReleaseGuard AI

AI-assisted release intelligence for SQL and Oracle environments.

---

## Dashboard Preview

![Release Dashboard](screenshots/release-dashboard.png)
<img width="1536" height="587" alt="release-dashboard" src="https://github.com/user-attachments/assets/a8121e1e-e817-4555-8f6c-829b8e9b0af3" />


![Release Dashboard 2](screenshots/release-dashboard2.png)
<img width="485" height="386" alt="release-dashboard2" src="https://github.com/user-attachments/assets/43c7a488-2bbd-4cc1-88cf-c0bbb0e1bf7f" />

---

## Dependencies & Impact Analysis

![Dependencies](screenshots/release-dependencies.png)
<img width="491" height="613" alt="release-dependencies" src="https://github.com/user-attachments/assets/fee6278e-35ba-4985-8efe-4bc5c68b8f86" />

---

## Problem

Many enterprise teams still validate database releases manually.

This creates:

- production risk
- undocumented changes
- permission issues
- broken dependencies
- slow release cycles

## What ReleaseGuard AI does

ReleaseGuard AI analyzes SQL release scripts and generates automated release intelligence reports.

## Current concept features

- SQL impact analysis
- Permission change detection
- AI-generated summaries
- Changelog generation
- Risk scoring
- Dependency analysis

## Example input

```sql
ALTER TABLE POLICY_CUSTOMERS
ADD EMAIL VARCHAR2(200);

GRANT SELECT ON POLICY_CUSTOMERS TO REPORTING_ROLE;
```

## Example output

```text
Affected objects:
- POLICY_CUSTOMERS

Detected changes:
- New column: EMAIL
- Permission change detected

Potential risks:
- Sensitive field introduced
- Reporting access expanded

Suggested validations:
- Check ETL mappings
- Validate masking policies

Risk level: LOW
```

## Architecture

```text
SQL Scripts
    ↓
Parser Engine
    ↓
Impact Analyzer
    ↓
Risk Detection
    ↓
AI Summary Layer
    ↓
Release Intelligence Report
```

## Documentation

See:
sample-analysis.md
architecture.md
roadmap.md


## Roadmap

- Oracle parser
- Changelog generator
- Risk engine
- Dependency graph
- GitHub Actions integration# releaseguard-ai
AI-assisted SQL release intelligence for enterprise database deployments.
