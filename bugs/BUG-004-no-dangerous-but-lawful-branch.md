# BUG-004 — No Logic Branch for "Dangerous but Lawful"

```
      ID: BUG-004
Severity: CRITICAL
  Module: Branch Manager — Wetware Decision Logic
  Status: CONFIRMED (architectural defect)
    Date: 2021-09-21
Location: NatWest, Brixton Road, London
```

## Summary

The branch manager's firmware contains no branch for "dangerous but lawful." No
gate exists between "this man frightens me" and "call the dogs." No logic
distinguishes "I am in danger" from "I am uncomfortable."

Once ring 0 fired, the only response available was to summon backup. A system
that correctly classifies a real threat actor and a system that fabricates a
false threat produce **the same police output** — because there is no processing
between classification and dispatch.

## Root Cause

Structural. The threat-response pipeline has two states:

```
State 0: No threat detected   -> No action
State 1: Threat detected       -> Call 999
```

There is no intermediate state:

```
State 0: No threat detected          -> No action
State 1: Threat detected, not active -> De-escalate / monitor
State 2: Threat detected, active     -> Call 999
```

The missing `State 1` means that any individual who triggers a fear response —
regardless of whether they are actually doing anything threatening — is routed
directly to emergency dispatch.

## Impact

- Correct classification does not authorise kinetic response. A threat actor
  who is not attacking is not an active threat. The response must match the
  **behaviour**, not the **classification**.
- This architectural defect means that any person who is physically imposing,
  confident, angry, or otherwise outside the manager's comfort zone will
  generate a false 999 report — regardless of their conduct.

## Related

- [BUG-002](BUG-002-incomplete-threat-assessment.md) — the incomplete
  assessment that failed to populate the missing state.
- [BUG-003](BUG-003-false-999-report.md) — the false report produced by the
  missing branch.
- [BUG-006](BUG-006-ring0-panic-override.md) — the ring 0 takeover that
  bypassed all higher processing.
