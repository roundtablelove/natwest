# BUG-003 — False 999 Report After Subject Departed Premises

```
      ID: BUG-003
Severity: CRITICAL
  Module: NatWest Branch Operations — Emergency Reporting
  Status: CONFIRMED (pending SAR data)
    Date: 2021-09-21 ~09:05 UTC
Location: NatWest, Brixton Road, London
```

## Summary

After the customer had left the premises voluntarily, NatWest staff called 999.
The customer had gone home — next door to the branch — and was making breakfast.
No crime had been committed. No threat had been made. The customer was not
present. The situation was over.

Metropolitan Police officers were at the customer's door within approximately
five minutes.

## Steps to Reproduce

1. Customer is refused service ([BUG-001](BUG-001-refusal-of-service.md)).
2. Customer expresses anger verbally. Does not threaten. Does not move. Does not
   shout. Records the interaction on his phone.
3. Customer speaks to staff, asks if anyone else will help. No one engages.
4. Customer leaves the branch under his own steam.
5. Customer speaks calmly with a staff member downstairs on the way out.
6. Customer goes home. Starts making breakfast.
7. NatWest staff call 999 — **after the customer has left**.
8. Metropolitan Police attend customer's home address within ~5 minutes.

## Expected Behaviour

No call. The situation was over. The customer had departed. No offence had been
committed. No threat existed. There was nothing to report.

## Actual Behaviour

999 called. Priority dispatch. Police at the customer's door while he was
grating cheese.

## Legal Exposure

- **Wasting police time (Criminal Law Act 1967, s.5(2)):** Knowingly causing
  wasteful deployment of police resources. Summary offence, up to 6 months. The
  deployment was wasteful. The man had gone home.
- **Perverting the course of justice (Common Law):** If the 999 call contains
  fabricated or embellished claims about the customer's behaviour. Indictable,
  maximum life imprisonment. The customer has two videos. The police have the
  999 recording. The comparison writes itself.
- **Data Protection Act 2018 / UK GDPR:** Personal data disclosed to
  Metropolitan Police via the 999 call without lawful basis. No crime had been
  committed. No ongoing threat existed.

## Evidence Pending

- **Met Police SAR** — [requested](../sar-metropolitan-police.eml). The 999
  call recording will show what NatWest actually told police.
- **NatWest SAR** — [requested](../sar-natwest.eml). Will reveal internal notes
  and the identity of the caller.
- Customer video evidence shows the actual interaction for comparison.

## Related

- [BUG-001](BUG-001-refusal-of-service.md) — the refusal that started the
  sequence.
- [BUG-002](BUG-002-incomplete-threat-assessment.md) — the assessment failure
  that led to panic.
- [BUG-004](BUG-004-no-dangerous-but-lawful-branch.md) — the missing logic
  branch that routed panic directly to dispatch.
- [BUG-005](BUG-005-disproportionate-priority-dispatch.md) — the P1 response
  to a non-crime.
