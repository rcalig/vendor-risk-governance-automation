## Flow Triggering

The workflow runs on a scheduled basis aligned to governance cadence e.g. daily.

The schedule ensures reassessment start dates are detected promptly
without generating unnecessary execution noise.

## Data Retrieval

## Data Retrieval

Only governance-relevant attributes are retrieved, including:
- Vendor identifier and name
- Risk tier
- Assessment status
- Last assessment date
- Reassessment start date

No assessment artefacts, evidence, or platform-specific metadata are ingested.

## Reassessment Evaluation Logic

For each vendor, the automation evaluates:
- Whether a reassessment start date exists
- Whether the start date matches the current operating day
- Whether the vendor is already under reassessment

This logic is implemented upstream to ensure consistent interpretation
and auditability.

## Exception Aggregation and Notification

Rather than generating individual alerts:
- Vendors meeting reassessment criteria are aggregated
- A single summary notification is produced
- Notifications are sent only when action is required

This approach avoids alert fatigue and focuses attention on execution.

## Data Staging

A structured CSV extract is generated as the authoritative reporting input.

The extract:
- Represents a point-in-time governance state
- Is human-readable and auditable
- Decouples reporting from the source system





