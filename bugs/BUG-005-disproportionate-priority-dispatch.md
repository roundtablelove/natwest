# BUG-005 — Disproportionate Priority Dispatch for Non-Crime

```
      ID: BUG-005
Severity: HIGH
  Module: Metropolitan Police — Dispatch Prioritisation
  Status: CONFIRMED (pending SAR data)
    Date: 2021-09-21 ~09:05 UTC
Location: Brixton, London
```

## Summary

Metropolitan Police assigned P1 (priority) dispatch to a call concerning a man
who had already left a bank premises, had committed no offence, and had made no
threat. Officers were at the customer's home address within approximately five
minutes — during Tuesday morning rush hour in Brixton.

If you get stabbed on Coldharbour Lane you will wait an hour. You could get shot
on Angel Town and the response time would be measured in coffee breaks. But a
bank manager whose ego got bruised by a man who wanted his own money — P1. Blue
lights. Rapid deployment for a customer who had gone home to make an omelette,
humming a tune.

## Root Cause

NatWest got a priority response that actual victims of actual crime in Brixton
do not get, for an incident that was not a crime, involving a man who was not
present, because one branch of Babylon called another and the request was
assigned P1 by default.

Corporate callers — particularly banks — receive automatic priority grading that
individual callers reporting actual violent crime do not.

## Evidence Pending

- **Met Police SAR** — [requested](../sar-metropolitan-police.eml). CAD record
  will show the grading assigned, dispatch time, and the information provided
  to attending officers.

## Related

- [BUG-003](BUG-003-false-999-report.md) — the false report that generated the
  dispatch.
- [BUG-004](BUG-004-no-dangerous-but-lawful-branch.md) — the missing logic
  branch that routed the report to 999 in the first place.
