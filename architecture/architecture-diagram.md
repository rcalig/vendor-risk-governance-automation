Vendor Risk Governance Data (API)
--------------------------------
- Vendor inventory
- Risk tier
- Assessment status
- Reassessment start date
(no evidence / no scores)
            |
            v
Automation (Governance Rules)
-----------------------------
- Date normalisation (timezone)
- Reassessment cadence by tier
- Start date = today
- Exception aggregation
[policy enforced here]
            |
            +--------------------+
            |                    |
            v                    v
Staged Extract (CSV)      Email / Notification
-------------------       --------------------
- Point-in-time snapshot  (summary only)
- Traceable               sent if count > 0
- Re-runnable
            |
            v
Executive Oversight (Power BI)
------------------------------
- Starting today
- Overdue
- Exceptions
Oversight ≠ Operations
