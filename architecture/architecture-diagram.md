## Architecture (Text view)

```text
+--------------------+   +--------------------+   +--------------------+
| Vendor Risk Data   |-->| Automation Rules   |-->| Exec Oversight     |
| (API)              |   | (Governance)       |   | (Power BI)         |
+--------------------+   +--------------------+   +--------------------+
                               |
                               v
                    +--------------------+
                    | Notification       |
                    | (summary only)     |
                    +--------------------+
                               |
                               v
                    +--------------------+
                    | Staged Extract     |
                    | (CSV snapshot)     |
                    +--------------------+

