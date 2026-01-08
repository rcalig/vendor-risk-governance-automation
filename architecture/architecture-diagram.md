┌──────────────────────────────┐
│  Vendor Risk Governance Data │
│            (API)             │
│                              │
│  - Vendor inventory          │
│  - Risk tier                 │
│  - Assessment status         │
│  - Reassessment start date   │
└───────────────┬──────────────┘
                │
                ▼
┌────────────────────────────────────────┐
│        Automation (Governance Rules)   │
│                                        │
│  - Date normalisation (timezone)       │
│  - Reassessment cadence by tier        │
│  - Start date = today check            │
│  - Exception aggregation               │
│                                        │
│            [policy enforced here]      │
└───────────────┬──────────────┬─────────┘
                │              │
                │              │  (conditional)
                │              ▼
                │     ┌──────────────────────┐
                │     │  Email / Notification│
                │     │     (summary only)   │
                │     │   sent if count > 0  │
                │     └──────────────────────┘
                │
                ▼
┌──────────────────────────────┐
│   Staged Extract (CSV)       │
│   - Point-in-time snapshot   │
│   - Traceable / re-runnable  │
└───────────────┬──────────────┘
                │
                ▼
┌──────────────────────────────┐
│     Executive Oversight      │
│         (Power BI)           │
│                              │
│  - Starting today            │
│  - Overdue                   │
│  - Exceptions                │
│                              │
│     Oversight ≠ Operations   │
└──────────────────────────────┘
