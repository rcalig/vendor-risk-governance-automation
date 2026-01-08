## Architecture (Text view)
+----------------------+   +----------------------+   +----------------------+
| Vendor Risk Data     |-->| Automation Rules     |-->| Executive Oversight  |
| (API)                |   |                      |   | (Power BI)           |
|                      |   | - Date normalisation |   |                      |
| - Inventory          |   | - Cadence by tier    |   | - Starting today     |
| - Risk tier          |   | - Start = today      |   | - Overdue            |
| - Status             |   | - Exception logic    |   | - Exceptions         |
| - Reassess start     |   |                      |   |                      |
+----------------------+   +----------+-----------+   +----------------------+
                                     |
                                     v
                          +----------------------+
                          | Notification         |
                          | (summary only)       |
                          +----------------------+
                                     |
                                     v
                          +----------------------+
                          | Staged Extract (CSV) |
                          | Point-in-time        |
                          +----------------------+
