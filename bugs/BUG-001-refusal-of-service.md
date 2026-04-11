# BUG-001 — Refusal of Service With Valid Government-Issued ID

```
      ID: BUG-001
Severity: HIGH
  Module: NatWest Branch Operations — Customer Service
  Status: CONFIRMED
    Date: 2021-09-21 08:59 UTC
Location: NatWest, Brixton Road, London
```

## Summary

Lifelong customer presenting valid government-issued photographic identification
(passport) was refused a cash withdrawal at his home branch. No lawful reason
for the refusal was communicated at the time or subsequently.

## Steps to Reproduce

1. Customer attends home branch (NatWest Brixton Road) — account held since
   childhood.
2. Customer presents valid UK passport as identification.
3. Customer requests cash withdrawal exceeding counter limit.
4. Customer is referred to branch manager.
5. Branch manager denies withdrawal.

## Expected Behaviour

Withdrawal processed. Customer has valid ID, a longstanding account in good
standing, and is attending his home branch. Standard verification procedures
should clear the transaction.

## Actual Behaviour

Withdrawal refused. No reason given. No alternative offered. No escalation path
communicated to customer.

## Regulatory Exposure

- **FCA Principle 6 (Treating Customers Fairly):** A lifelong customer was
  refused access to his own funds with valid ID at his home branch for no
  communicated reason.
- **FCA Principle 3 (Management and Control):** The refusal appears to be an
  individual management decision unsupported by policy or procedure.

## Evidence

- Video 1 — customer states on camera that he has been refused his money.
  Branch staff do not dispute this. ([PXL_20210921_085956653.mp4](../PXL_20210921_085956653.mp4))
- Video 2 — customer repeats the complaint to a staff member downstairs, calmly
  and without aggression. ([PXL_20210921_090033002.mp4](../PXL_20210921_090033002.mp4))

## Related

- [BUG-002](BUG-002-incomplete-threat-assessment.md) — the refusal preceded and
  triggered the threat assessment failure.
- [BUG-003](BUG-003-false-999-report.md) — the false report followed the
  refusal.
- [Formal complaint to NatWest](../complaint-natwest.eml)
