## Architecture Overview

The architecture is intentionally simple and modular.

Vendor risk governance data (vendor inventory, assessment status, and reassessment
cadence) is sourced via API from an external system and processed through a
lightweight automation layer.

The output is a stable, traceable reporting extract consumed by Power BI
for executive oversight.

## Rationale

Governance rules are enforced upstream, outside the reporting layer.

This ensures reassessment cadence and tier-based rules are applied consistently
and remain auditable. The reporting layer is therefore stable, explainable,
and suitable for executive consumption.

Separating governance logic from reporting reduces operational risk introduced
by ad-hoc calculations embedded in dashboards.

