## Architecture (Text view)

+-------------------------------+     +-----------------------------------+     +------------------------------+
| Vendor Risk Governance Data   | --> | Automation (Governance Rules)      | --> | Executive Oversight           |
| (API)                         |     |                                   |     | (Power BI)                   |
|                               |     | - Date normalisation (timezone)   |     |                              |
| - Vendor inventory            |     | - Reassessment cadence by tier   |     | - Starting today             |
| - Risk tier                   |     | - Start date = today             |     | - Overdue                    |
| - Assessment status           |     | - Exception aggregation          |     | - Exceptions                 |
| - Reassessment start date     |     |                                   |     |                              |
|                               |     | [policy enforced here]           |     |                               |
| (no evidence / no scores)     |     +------------------+----------------+     +------------------------------+
+-------------------------------+                        |
                                                           |
                                                           v
                                         +-----------------------------------+
                                         | Email / Notification              |
                                         | (summary only)                    |
                                         | sent if count > 0                 |
                                         +-----------------------------------+

                     +-----------------------------------+
                     | Staged Extract (CSV)              |
                     |                                   |
                     | - Point-in-time snapshot          |
                     | - Traceable                       |
                     | - Re-runnable                     |
                     +-----------------------------------+

