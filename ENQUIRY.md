# Enquiry: Pattern of False Reporting — NatWest Brixton Road

```
 Enquiry ID: ENQ-20210921-001
    Relates: IR-20210921-NATWEST
      Scope: NatWest Brixton Road branch — historical pattern of false or
             disproportionate 999 calls resulting in arrest or charge of
             customers
     Status: OPEN
```

## 1. Purpose

The defects identified in [IR-20210921-NATWEST](README.md) are structural, not
personal. [BUG-004](bugs/BUG-004-no-dangerous-but-lawful-branch.md) — the
absence of a logic branch for "dangerous but lawful" — is an architectural
defect. It does not exist only in one manager's firmware. If the branch's
operating culture, training, and escalation procedures contain this defect, then
it has fired before.

The question is not whether this has happened to other people. The question is
how many, and what happened to them.

The complainant in IR-20210921 went home, made breakfast, and had the police at
his door within five minutes. He was not arrested. He was not charged. He had
video evidence. He had a flat next door. He is articulate, legally aware, and
capable of mounting a defence.

Not everyone who walks into NatWest Brixton Road has those advantages.

## 2. Questions

### 2.1. Has NatWest Brixton Road Made Other 999 Calls About Customers?

- How many 999 calls has NatWest Brixton Road made in the last 10 years?
- What was the nature of each call?
- How many involved a customer who had already left the premises at the time of
  the call?
- How many involved a customer who had committed no criminal offence?
- How many resulted in police attendance at the customer's home or place of
  work?

### 2.2. Have People Been Arrested?

- How many of those 999 calls resulted in arrest?
- What were the stated grounds for arrest in each case?
- How many of those arrested were charged?
- How many of those charged were convicted?
- How many were released without charge?
- How many had charges dropped before trial?
- How many were acquitted at trial?

### 2.3. What Happened to the People Who Were Arrested?

An arrest is not nothing. Even without charge, an arrest means:

- Physical detention — handcuffs, cell, processing.
- A custody record — permanent. Disclosed on enhanced DBS checks.
- DNA and fingerprints taken — retained on the national database.
- Potential loss of employment — many employers terminate on arrest, not
  conviction.
- Psychological harm — particularly for people who have never been in custody.
- Reputational damage — neighbours see the police. Colleagues hear rumours.

For those who were charged:

- Court appearances — time, cost, stress, public record.
- Legal fees — even if acquitted, the cost of defence is not recovered.
- Potential conviction — a criminal record, for an incident that was not a
  crime.
- Custodial sentence — if convicted and sentenced to imprisonment, for an
  incident that was not a crime.

### 2.4. Who Were These People?

- What is the demographic breakdown (age, sex, ethnicity) of customers against
  whom NatWest Brixton Road has made 999 calls?
- Is there a pattern? Brixton's population is disproportionately Black. If the
  999 calls disproportionately target Black customers, this is not a customer
  service failure — it is institutional racism operationalised through the
  emergency services.
- How many of these customers were, like the complainant, presenting valid ID
  and requesting access to their own money?

### 2.5. Is This Branch an Outlier?

- How does NatWest Brixton Road's rate of 999 calls compare to other NatWest
  branches of similar size and footfall?
- How does it compare to other banks on Brixton Road?
- Is the rate consistent over time, or did it change with specific managers or
  staff?

## 3. Data Sources

### 3.1. Metropolitan Police

The Met holds dispatch records for every 999 call. A Freedom of Information
request or data analytics query can establish:

| Data Point | Source |
| :--- | :--- |
| Number of 999 calls from NatWest Brixton Road, last 10 years | CAD records |
| Dispatch grading for each call | CAD records |
| Outcome of each dispatch (arrest / no arrest / no crime) | Crime reports, CRIS |
| Charges brought | CPS referral records |
| Convictions | Court outcomes |
| Demographic data of subjects | Custody records |

**Request:** Freedom of Information Act 2000, s.1 — all records of 999 calls
originating from NatWest, Brixton Road, London for the period 2011–2021,
including CAD records, dispatch outcomes, arrest records, and charge outcomes.

### 3.2. NatWest

NatWest holds internal incident logs, security reports, and staff training
records.

| Data Point | Source |
| :--- | :--- |
| Number of security incidents logged at Brixton Road branch | Internal incident log |
| Number of 999 calls made by branch staff | Security records |
| Staff involved in each incident | HR / management records |
| Training records — de-escalation, threat assessment | HR / training records |
| Complaints received from customers about similar incidents | Complaints register |

**Request:** Subject Access Request (existing — [sar-natwest.eml](sar-natwest.eml))
covers the complainant's own data. A broader FOI-equivalent request via the FCA
or a court disclosure order would be needed for systemic data.

### 3.3. Financial Ombudsman Service

The FOS holds records of complaints against NatWest Brixton Road.

| Data Point | Source |
| :--- | :--- |
| Complaints about refusal of service | FOS case records |
| Complaints about police being called on customers | FOS case records |
| Complaints about discriminatory treatment | FOS case records |

### 3.4. Independent Office for Police Conduct (IOPC)

If officers arrested people on the basis of false or exaggerated 999 calls from
NatWest, the IOPC may hold:

| Data Point | Source |
| :--- | :--- |
| Complaints about arrests arising from NatWest Brixton Road calls | IOPC records |
| Investigations into disproportionate response | IOPC records |

## 4. Known Incidents

### 4.1. Mr C — Arrested in Own Bank, Photo ID Dispute

```
   Witness: Mr C (details pending — contact not yet established)
  Location: Bank branch in Brixton (branch to be confirmed)
   Allegation: Customer arrested inside bank because staff claimed he did
               not match his own photo ID. He did.
    Status: AWAITING CONTACT
```

A known associate of the complainant was arrested inside a bank branch in
Brixton after staff claimed he did not match his own photograph on his
identification document. He did match. He was arrested anyway.

This is a direct instance of the pattern under investigation. The same
pipeline:

```
CLASSIFY: Customer does not look right.
ASSESS:   [NONE — or conclusion predetermined]
RESPONSE: Call police.
OUTCOME:  Arrested. In his own bank. For looking like himself.
```

If this occurred at NatWest Brixton Road, it is a second confirmed firing of
[BUG-004](bugs/BUG-004-no-dangerous-but-lawful-branch.md) — except worse. In
the complainant's case (IR-20210921), at least an interaction occurred. In Mr
C's case, the classification itself was false. He matched his photo. They said
he didn't. This is not a ring 0 panic. This is either incompetence or
fabrication.

**Details pending.** Mr C does not answer his phone. He will be contacted and
this section updated with:

- Full name (with consent)
- Date of incident
- Which bank / which branch
- Whether he was charged
- Outcome
- Whether he has video, witnesses, or documentation

> Mr C. Call me.

---

## 5. Hypotheses

### 5.1. Isolated Incident

The incident on 21 September 2021 was a one-off failure by one manager on one
day. The defects are personal to that manager. The branch does not have a
systemic problem.

**If true:** The data will show that NatWest Brixton Road makes 999 calls
rarely, in line with comparable branches, and that calls result in justified
police action.

### 5.2. Systemic Pattern — Operational

The branch has a culture of calling 999 as a first resort when staff feel
uncomfortable. The defects identified in [BUG-004](bugs/BUG-004-no-dangerous-but-lawful-branch.md)
and [BUG-006](bugs/BUG-006-ring0-panic-override.md) are present in the
branch's training, procedures, and culture, not just in one manager's firmware.
Multiple customers have been subjected to false reports. Some have been arrested.
Some have been charged. Some may have been convicted — for incidents that were
not crimes.

**If true:** The data will show an elevated rate of 999 calls, a low rate of
subsequent charge and conviction, and a pattern of calls made after the customer
has left or where no offence was committed.

### 5.3. Systemic Pattern — Discriminatory

As 4.2, but with a demographic skew. The branch disproportionately targets
Black customers, young men, or people who do not present as middle-class. The
emergency services are being used as an enforcement arm for racial or class
profiling.

**If true:** The data will show a demographic pattern in the subjects of 999
calls that does not match the branch's customer demographics.

## 6. Actions

| # | Action | Status |
| :--- | :--- | :--- |
| 1 | Draft FOI request to Metropolitan Police — 999 calls from NatWest Brixton Road (2011–2021) | PENDING |
| 2 | Draft FOI request to Metropolitan Police — arrest and charge outcomes arising from those calls | PENDING |
| 3 | Request FOS complaint history for NatWest Brixton Road | PENDING |
| 4 | Request IOPC records relating to arrests arising from NatWest Brixton Road 999 calls | PENDING |
| 5 | Analyse demographic data if obtained | BLOCKED (#1, #2) |
| 6 | Compare NatWest Brixton Road 999 call rate with comparable branches | BLOCKED (#1) |
| 7 | Identify other affected customers | BLOCKED (#1, #2) |
| 8 | If pattern confirmed — refer to Equality and Human Rights Commission | BLOCKED (#5) |
| 9 | Contact Mr C — obtain incident details, dates, branch, outcome | PENDING |

## 7. Why This Matters

The complainant was not arrested. He had video. He had a home next door. He
knew his rights.

Someone else who walked into that branch — someone without a phone, without
legal knowledge, without a home next door, without the confidence to challenge
— could have been arrested on the basis of a false report, charged on the basis
of fabricated or embellished claims, and convicted on the basis of a bank
manager's word against theirs.

If that has happened, those people have criminal records for crimes that did not
occur. They may have served time. They may have lost jobs, housing, custody of
children. They may have had their lives destroyed because a bank manager felt
uncomfortable and the system has no gate between "I am uncomfortable" and "send
the dogs."

The defect in [BUG-004](bugs/BUG-004-no-dangerous-but-lawful-branch.md) does
not need to fire many times to ruin lives. It only needs to fire once per
person.

---

## Related

- [Incident Report — IR-20210921-NATWEST](README.md)
- [BUG-003 — False 999 report after subject departed](bugs/BUG-003-false-999-report.md)
- [BUG-004 — No logic branch for "dangerous but lawful"](bugs/BUG-004-no-dangerous-but-lawful-branch.md)
- [BUG-005 — Disproportionate priority dispatch](bugs/BUG-005-disproportionate-priority-dispatch.md)
- [BUG-006 — Ring 0 panic override produces false report](bugs/BUG-006-ring0-panic-override.md)
