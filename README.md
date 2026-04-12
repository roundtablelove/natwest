# Incident Report: NatWest Brixton Road — 21 September 2021

```
  Report ID: IR-20210921-NATWEST
       Date: Tuesday 21 September 2021, 08:59 UTC
   Location: NatWest, Brixton Road, London (adjacent to complainant's home)
    Subject: Refusal of service, false 999 report, disproportionate police dispatch
 Complainant: Arthur Douglas Noel
     Status: OPEN — SAR responses pending
```

## 1. Executive Summary

On 21 September 2021 at approximately 08:59 UTC, the complainant attended his
home branch of NatWest (Brixton Road, London) to withdraw cash from his own
account. He presented valid government-issued photographic identification (UK
passport). He has held an account at this branch since childhood.

The branch manager refused the withdrawal without providing a lawful reason.
The complainant expressed anger verbally. He did not threaten anyone, did not
raise his voice to a shout, did not move toward anyone. He recorded the
interaction on his phone and left the premises voluntarily.

After the complainant had left and gone home (next door), NatWest staff called
999. Metropolitan Police attended his home address within approximately five
minutes. No crime had been committed. No threat had been made. The complainant
was making breakfast.

Seven defects have been identified. See [Section 6 — Defect Register](#6-defect-register).

---

## 2. Background

The complainant was 2 days out of custody after ten days on remand (false
charges — subsequently not pursued). Prison collapses the processing stack.
Every higher function — planning, abstraction, strategic thinking — is a luxury
that depends on safety. In a prison environment there is no safety. The nervous
system shuts down higher rings and routes everything through ring 0: threat
detection, social calibration, immediate response.

On release, the stack does not automatically reinitialise. The body is out but
the nervous system remains in survival mode. Ring 0 stays in command.

The complainant was operating without a persona layer. No customer-service
smile. No filter. Raw.

His wallet was lost or stolen during arrest and detention. He attended the
branch carrying his passport as ID and requested a cash withdrawal exceeding
the counter limit. He was referred to the branch manager.

---

## 3. Timeline

| Time (UTC) | Event |
| :--- | :--- |
| ~08:59 | Complainant attends NatWest Brixton Road with passport as ID. |
| ~09:00 | Referred to branch manager for withdrawal exceeding counter limit. |
| ~09:00 | Manager refuses withdrawal. No reason given. ([BUG-001](bugs/BUG-001-refusal-of-service.md)) |
| ~09:00 | Manager's threat assessment classifies complainant correctly but aborts before completion. Provokes instead. ([BUG-002](bugs/BUG-002-incomplete-threat-assessment.md)) |
| ~09:01 | Complainant expresses anger verbally. Does not threaten, shout, or move. Manager experiences ring 0 panic, flees to office. ([BUG-006](bugs/BUG-006-ring0-panic-override.md)) |
| ~09:01 | Complainant records interaction on phone (Video 1, 21 seconds). |
| ~09:02 | Complainant speaks to remaining staff on camera. No one engages. |
| ~09:02 | Complainant leaves the branch floor. |
| ~09:03 | Complainant speaks calmly with a female staff member downstairs. Not threatened. |
| ~09:04 | Complainant exits branch. Goes home (next door). Starts making breakfast. |
| ~09:05 | NatWest staff call 999. Complainant is no longer on premises. ([BUG-003](bugs/BUG-003-false-999-report.md)) |
| ~09:10 | Metropolitan Police attend complainant's home address. ([BUG-005](bugs/BUG-005-disproportionate-priority-dispatch.md)) |

---

## 4. Evidence

### 4.1. Video 1 — The Branch (21 seconds)

[![Video 1 — the branch](manager.png)](PXL_20210921_085956653.mp4)

**Transcript:**

> **[00:00] Complainant to Manager:** So you're saying you're not gonna let me
> take my money out of my bank, are you? Wow, you really are an arsehole.
>
> **[00:07] Complainant to Staff:** Ah... Excuse me. Are any of you guys gonna
> let me take my money out? Cuz this guy... if you hear that. I have not been
> aggressive. I've done nothing. I just want my money. You gonna help me?
>
> **[00:12] Staff Member to Complainant:** [Unintelligible].
>
> **[00:15] Complainant to Staff:** So the manager is [half laugh] not letting
> me take the money out and you guys agree with that?
>
> **[00:17] Staff Member to Complainant:** Are you filming me?
>
> **[00:19] Complainant to Staff Member:** Of course I am.
>
> **[00:19] Complainant to Staff:** Right, I'll see you guys.

**Stills:**

| [00:01] The Manager | [00:02] Fleeing |
| :---: | :---: |
| ![The Manager](manager.png) | ![Fleeing](manager-fleeing-1.png) |
| **[00:02] Gone** | **[00:16] Staff Member** |
| ![Gone](manager-fleeing-2.png) | ![Staff Member](fake-rude-bwoy.png) |

**Assessment of tone:** First line is spoken with anger — addressed to the
manager. From [00:07] the anger is gone. The complainant is speaking to the
remaining staff calmly, clearly, making a record. He states on camera that he
has not been aggressive. None of the staff engage with the substance.

Note: the manager is already in motion at the start of the video. The
complainant is seated throughout. The manager is fleeing. The complainant is not
pursuing. At no point does he raise his voice to a shout, make a threat, or move
toward anyone. He leaves under his own steam.

### 4.2. Video 2 — Departure (Stairs)

[![Video 2 — departure](manager-fleeing-1.png)](PXL_20210921_090033002.mp4)

The complainant walks down the stairs, humming. No anger. No menace. He says to
a staff member in passing:

> Do you know, your manager is refusing to let me take my money. It's nuts.
> Utterly nuts.

He then spoke with a female staff member downstairs (who was not threatened by
him) for a couple of minutes before leaving the branch and going home.

### 4.3. Pending Evidence

| Item | Source | Status |
| :--- | :--- | :--- |
| 999 call recording | Met Police SAR ([requested](sar-metropolitan-police.eml)) | PENDING |
| CAD record and dispatch log | Met Police SAR | PENDING |
| Body-worn video from attending officers | Met Police SAR | PENDING |
| NatWest internal incident notes | NatWest SAR ([requested](sar-natwest.eml)) | PENDING |
| CCTV footage from branch | NatWest SAR | PENDING |
| Identity of 999 caller | NatWest SAR | PENDING |

---

## 5. Analysis

### 5.1. The Core Logic Error

The manager's firmware correctly classified the complainant as a man of
significant power. The classification was accurate. The error is structural:
the manager's firmware has no branch for "dangerous but lawful." No gate between
"this man frightens me" and "call the dogs." No logic to distinguish "I am in
danger" from "I am uncomfortable." Once ring 0 fired, the only response
available was to summon backup.

A system that correctly classifies a real threat actor and a system that
fabricates a false threat produce the same police output — because there is no
processing between classification and dispatch.
([BUG-004](bugs/BUG-004-no-dangerous-but-lawful-branch.md))

### 5.2. What Should Have Happened

```
CLASSIFY: Power. Warrior class.
ASSESS:   Customer is angry, not hostile. No threat made.
          No physical movement. No weapon. Voice controlled.
          Anger is directed at policy, not at person.
RESPONSE: De-escalate. Process the withdrawal. Apologise.
```

### 5.3. What Actually Happened

```
CLASSIFY: Power. Warrior class.
ASSESS:   [INCOMPLETE — assessment aborted by ego]
PROVOKE:  Deny service. Assert borrowed authority over real authority.
RESULT:   Customer shows tooth.
PANIC:    Ring 0 takeover. Primal fear. Flee.
RESPONSE: Call 999. Report man who has already left.
```

### 5.4. The False Report

The complainant made no threat. Did not move a muscle. He showed the hint of
anger and called the manager an arsehole. He then left. The manager called 999
after the situation was over, about a man who was no longer present, in respect
of an incident that was not a crime.

NatWest received a priority police response that actual victims of actual
violent crime in Brixton do not receive.

---

## 6. Defect Register

| ID | Severity | Title | File |
| :--- | :--- | :--- | :--- |
| BUG-001 | HIGH | Refusal of service with valid government-issued ID | [BUG-001](bugs/BUG-001-refusal-of-service.md) |
| BUG-002 | CRITICAL | Incomplete threat assessment before provocation | [BUG-002](bugs/BUG-002-incomplete-threat-assessment.md) |
| BUG-003 | CRITICAL | False 999 report after subject departed premises | [BUG-003](bugs/BUG-003-false-999-report.md) |
| BUG-004 | CRITICAL | No logic branch for "dangerous but lawful" | [BUG-004](bugs/BUG-004-no-dangerous-but-lawful-branch.md) |
| BUG-005 | HIGH | Disproportionate priority dispatch for non-crime | [BUG-005](bugs/BUG-005-disproportionate-priority-dispatch.md) |
| BUG-006 | CRITICAL | Ring 0 panic override produces false report | [BUG-006](bugs/BUG-006-ring0-panic-override.md) |
| BUG-007 | MEDIUM | Fake rude bwoy intimidation display | [BUG-007](bugs/BUG-007-fake-rude-bwoy.md) |

---

## 7. Legal Exposure — NatWest

### 7.1. Criminal

- **Wasting police time (Criminal Law Act 1967, s.5(2))** — knowingly causing
  wasteful deployment of police resources. Summary offence, up to 6 months.
  ([BUG-003](bugs/BUG-003-false-999-report.md))
- **Perverting the course of justice (Common Law)** — if the 999 call contains
  fabricated or embellished claims about the complainant's behaviour. Indictable,
  maximum life imprisonment. The complainant has two videos. The police have the
  999 recording. The comparison writes itself.
  ([BUG-003](bugs/BUG-003-false-999-report.md))

### 7.2. Regulatory

- **FCA Principle 6 (Treating Customers Fairly)** — refusal of service with
  valid ID at home branch. ([BUG-001](bugs/BUG-001-refusal-of-service.md))
- **FCA Principle 3 (Management and Control)** — the decision to call 999 after
  the complainant had left suggests a failure of management judgement.
  ([BUG-003](bugs/BUG-003-false-999-report.md))

### 7.3. Data Protection

- **UK GDPR / DPA 2018** — personal data disclosed to Metropolitan Police via
  999 without lawful basis. No crime committed, no ongoing threat.
  ([BUG-003](bugs/BUG-003-false-999-report.md))

### 7.4. The Overdraft (£4,000)

The complainant moved to another bank after the incident. He took all his cash
plus a £4,000 overdraft as partial compensation for the refusal of service and
the false report. [Civil action](complaint-natwest.eml) is pending. He
acknowledges that damages sought must be net of this figure. He will not pay
interest.

---

## 8. Actions Pending

| # | Action | Depends On | Status |
| :--- | :--- | :--- | :--- |
| 1 | Met Police SAR — obtain 999 call recording, CAD, BWV | — | PENDING |
| 2 | NatWest SAR — obtain account notes, CCTV, incident log | — | PENDING |
| 3 | Identify downstairs witness (female staff member) | — | PENDING |
| 4 | Compare 999 recording with video evidence | #1, #2 | BLOCKED |
| 5 | Civil action against NatWest | #1, #2 | PENDING |
| 6 | FCA complaint if NatWest response unsatisfactory | #5 | PENDING |
| 7 | **[Pattern enquiry](ENQUIRY.md)** — establish whether NatWest Brixton Road has made false reports before, whether people have been arrested, charged, or convicted | — | OPEN |

---

## 9. Lessons Identified

1. **Correct classification does not authorise kinetic response.** A threat
   actor who is not attacking is not an active threat. The response must match
   the behaviour, not the classification.
   ([BUG-004](bugs/BUG-004-no-dangerous-but-lawful-branch.md))

2. **Complete the assessment before engaging.** The manager identified power,
   then provoked without following the thought. If you identify a wolf, do not
   poke it and then act surprised when it shows a tooth.
   ([BUG-002](bugs/BUG-002-incomplete-threat-assessment.md))

3. **Borrowed authority collapses under contact with real authority.** The
   manager's Babylon-issued authority evaporated the moment he faced a man whose
   authority is ancestral, not institutional.
   ([BUG-002](bugs/BUG-002-incomplete-threat-assessment.md))

4. **Ring 0 fear produces false reports.** When primal fear takes over, the
   organism calls for backup regardless of whether the threat is active. The
   police become an extension of one man's panic response — dispatched on the
   basis of a frightened man's ring 0, not on the basis of evidence.
   ([BUG-006](bugs/BUG-006-ring0-panic-override.md))

5. **The downstairs staff member is a witness.** She saw the complainant in
   conversation, calm, not threatening. She needs to be identified.

---

## Related Documents

- [Formal complaint to NatWest](complaint-natwest.eml)
- [Subject Access Request — Metropolitan Police](sar-metropolitan-police.eml)
- [Subject Access Request — NatWest](sar-natwest.eml)
- [Pattern Enquiry — Has this happened before?](ENQUIRY.md)

## Defect Reports

- [BUG-001 — Refusal of service with valid ID](bugs/BUG-001-refusal-of-service.md)
- [BUG-002 — Incomplete threat assessment before provocation](bugs/BUG-002-incomplete-threat-assessment.md)
- [BUG-003 — False 999 report after subject departed](bugs/BUG-003-false-999-report.md)
- [BUG-004 — No logic branch for "dangerous but lawful"](bugs/BUG-004-no-dangerous-but-lawful-branch.md)
- [BUG-005 — Disproportionate priority dispatch](bugs/BUG-005-disproportionate-priority-dispatch.md)
- [BUG-006 — Ring 0 panic override produces false report](bugs/BUG-006-ring0-panic-override.md)
- [BUG-007 — Fake rude bwoy intimidation display](bugs/BUG-007-fake-rude-bwoy.md)
