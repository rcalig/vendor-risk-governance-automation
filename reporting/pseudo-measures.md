# Power BI – Pseudo DAX Measures

## Total Vendors
DISTINCTCOUNT(Vendors[VendorId])

## Starting Today
CALCULATE(
  DISTINCTCOUNT(Vendors[VendorId]),
  Vendors[ReassessmentStartDate] = TODAY()
)

## Overdue
CALCULATE(
  DISTINCTCOUNT(Vendors[VendorId]),
  Vendors[ReassessmentDueDate] < TODAY()
)
## Exceptions
[Starting Today] + [Overdue]
