# BUG-002 — Incomplete Threat Assessment Before Provocation

```
      ID: BUG-002
Severity: CRITICAL
  Module: Branch Manager — Wetware Threat Assessment
  Status: CONFIRMED
    Date: 2021-09-21 ~09:00 UTC
Location: NatWest, Brixton Road, London
```

## Summary

The branch manager's threat assessment pipeline executed Stage 1 (classification)
correctly but aborted before completing Stage 2 (assessment). The manager then
initiated a provocation (refusal of service / dominance assertion) against a
correctly classified apex-level threat actor without evaluating the consequences.

This is a three-stage cascading failure:

1. **Classification: KING.** The manager's wetware correctly identified the
   customer as a man of power. Not "angry customer." Not "difficult bloke."
   Royalty. His firmware recognised it the way a dog recognises a wolf. The
   assessment was accurate.

2. **Provocation without follow-through.** Having correctly classified the
   customer as a king, the manager did not complete the assessment. Kings are
   apex killers. Have to be. You do not hold a crown for a thousand years by
   being nice. The manager's firmware registered the power but did not follow
   the thought to its conclusion. He provoked the king without understanding
   what he was provoking.

3. **Primal fear, ring 0 takeover.** The customer showed the barest hint of
   anger. The mask was off. The manager's wetware finally completed the
   assessment it should have run before the provocation: he was looking at an
   apex killer and he had just made him angry. Primal fear took over. Ring 0
   seized command. Whatever logic existed in higher mind was now irrelevant —
   the manager was operating on pure survival firmware.

## Root Cause

The assessment was aborted by ego. The manager's borrowed authority (Babylon-
issued, institutional) was challenged by contact with real authority (ancestral,
not institutional). The ego required a dominance assertion before the threat
assessment could complete. This inserted a provocation into the middle of an
incomplete evaluation — the critical error.

## Expected Behaviour

```
CLASSIFY: King. Apex predator. Warrior class.
ASSESS:   Customer is angry, not hostile. No threat made.
          No physical movement. No weapon. Voice controlled.
          Anger is directed at policy, not at person.
RESPONSE: De-escalate. Process the withdrawal. Apologise.
```

## Actual Behaviour

```
CLASSIFY: King. Apex predator. Warrior class.
ASSESS:   [INCOMPLETE — assessment aborted by ego]
PROVOKE:  Deny service. Assert borrowed authority over real authority.
RESULT:   King shows tooth.
PANIC:    Ring 0 takeover. Primal fear. Flee.
RESPONSE: Call 999. Report man who has already left.
```

## Evidence

- Video 1 — the manager is already in motion (fleeing) at the start of the
  recording. The customer is seated throughout. At no point does the customer
  raise his voice to a shout, make a threat, or move toward anyone.
  ([PXL_20210921_085956653.mp4](../PXL_20210921_085956653.mp4))
- Still frames: [manager.png](../manager.png),
  [manager-fleeing-1.png](../manager-fleeing-1.png),
  [manager-fleeing-2.png](../manager-fleeing-2.png)

## Related

- [BUG-001](BUG-001-refusal-of-service.md) — the refusal that initiated the
  provocation.
- [BUG-003](BUG-003-false-999-report.md) — the false report that followed the
  panic.
- [BUG-004](BUG-004-no-dangerous-but-lawful-branch.md) — the structural absence
  of a logic branch that would have prevented dispatch.
