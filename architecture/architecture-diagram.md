## Architecture at a glance

Vendor Risk Governance Data (API)
- Vendor inventory
- Risk tier
- Assessment status
- Reassessment start date
(no evidence / no scores)
        |
        v
Automation – Governance Rules
- Date normalisation (timezone)
- Reassessment cadence by tier
- Start date = today
- Exception aggregation
[policy enforced here]
        |
        |--(conditional)--> Email / Notification
        |                   (summary only, sent if count > 0)
        |
        v
Staged Extract (CSV)
- Point-in-time snapshot
- Traceable
- Re-runnable
        |
        v
Executive Oversight (Power BI)
- Starting today
- Overdue
- Exceptions
Oversight ≠ Operations

