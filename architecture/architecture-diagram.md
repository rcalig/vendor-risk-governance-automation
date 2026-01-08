## Architecture at a glance

| Stage | Purpose | Key Logic |
|------|--------|-----------|
| Vendor Risk Governance Data | Source of truth for vendor state | Inventory, tier, assessment status, reassessment start date |
| Automation (Governance Rules) | Enforces cadence and discipline | Timezone handling, tier-based rules, exception aggregation |
| Staged Extract (CSV) | Traceable reporting input | Point-in-time snapshot, re-runnable |
| Executive Oversight (Power BI) | Decision support | Starting today, overdue, exceptions |
| Notification (Conditional) | Operational prompt | Summary sent only if action is required |
