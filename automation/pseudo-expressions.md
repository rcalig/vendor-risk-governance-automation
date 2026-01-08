# Power Automate – Pseudo Expressions

These expressions illustrate vendor-agnostic automation patterns.
Field names are intentionally generic.

## Reassessment Start Date == Today

formatDateTime(
  convertTimeZone(utcNow(),'UTC','AUS Eastern Standard Time'),
  'yyyy-MM-dd'
)
and(
  not(empty(item()?['ReassessmentStartDate'])),
  equals(
    item()?['ReassessmentStartDate'],
    formatDateTime(
      convertTimeZone(utcNow(),'UTC','AUS Eastern Standard Time'),
      'yyyy-MM-dd'
    )
  )
)
## Notification Gate

greater(length(variables('VendorsToBeStarted')), 0)

## Tier-Based Cadence (Example)

addDays(
  item()?['ReassessmentStartDate'],
  if(
    equals(item()?['RiskTier'], 1), 120,
    if(
      equals(item()?['RiskTier'], 2), 60,
      if(
        equals(item()?['RiskTier'], 3), 30,
        0
      )
    )
  )
)
