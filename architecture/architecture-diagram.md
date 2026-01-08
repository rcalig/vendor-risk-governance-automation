## Architecture (Text view)

+----------------------------+     +-----------------------------+     +--------------------------+
| Vendor Risk Governance     | --> | Automation                  | --> | Executive Oversight       |
| Data (API)                 |     | (Governance Rules)          |     | (Power BI)               |
|                            |     |                             |     |                          |
| Inventory                  |     | - Date normalisation        |     | - Starting today         |
| Tier                        |     | - Cadence by tier           |     | - Overdue                |
| Assessment status           |     | - Start date = today        |     | - Exceptions             |
| Reassessment start date     |     | - Exception aggregation    |     |                          |
|                            |     | [policy enforced here]     |     | Oversight ≠ Operations   |
+----------------------------+     +--------------+--------------+     +--------------------------+
                                              |
                                              v
                               +-----------------------------+
                               | Notification (summary)      |
                               | sent only if action needed  |
                               +-----------------------------+

                               +-----------------------------+
                               | Staged Extract (CSV)        |
                               | point-in-time, traceable    |
                               +-----------------------------+

                     +-----------------------------------+
                     | Staged Extract (CSV)              |
                     |                                   |
                     | - Point-in-time snapshot          |
                     | - Traceable                       |
                     | - Re-runnable                     |
                     +-----------------------------------+

