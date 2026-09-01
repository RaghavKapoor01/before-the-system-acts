# Template 2 of 3 — Escalation Criteria in User Story Format

*Before the System Acts — Practitioner Framework for AI Governance Specification in Regulated Financial Services*

INVEST-compliant user stories translating each intervention threshold defined in the Decision Boundary Specification (Template 1, Section D) into backlog-ready requirements a development team can build and test against.

> **Purpose of this template:** This document is completed by the Business Analyst after the Decision Boundary Specification (Template 1) is signed off. Each mandatory human review, escalation, and pause condition named in Template 1, Section D becomes one user story here. The intervention threshold defines *what* must trigger review. This template defines *what the system and the reviewer must each do* when it does — in a form the development team can size, build, and test.

## A. Document Control

| Field | Notes |
|---|---|
| System / Initiative Name | Must match the linked Decision Boundary Specification |
| Linked Specification | Version and date of the Template 1 document this backlog is derived from |
| Version | Update on every material change |
| Business Analyst | Named author |
| Product Owner Sign-Off | Confirms these stories are backlog-ready |

## B. INVEST Compliance Check

*Before adding a story to the backlog, confirm it meets each condition. A story that fails any of these is not ready to build.*

| Criterion | Test |
|---|---|
| **Independent** | Can this story be built and tested without depending on another escalation story's completion? |
| **Negotiable** | Is the acceptance criteria specific enough to negotiate scope, without dictating implementation? |
| **Valuable** | Does this story trace to a named intervention threshold in Template 1 — not a generic "add logging" request? |
| **Estimable** | Can the development team size this without further clarification from the BA? |
| **Small** | Can this be built and tested within a single sprint? |
| **Testable** | Does the acceptance criteria specify a pass/fail condition a QA tester can execute without interpretation? |

## C. Escalation User Stories

*One user story per intervention threshold identified in Template 1, Section D. Do not combine multiple thresholds into one story — each threshold gets its own, even if the resulting stories look similar.*

### User Story 1

> As a **[role — e.g. first-line claims reviewer]**, when **[condition — e.g. model confidence falls below the threshold defined in Template 1, Section C1]**, I must **[action — e.g. review the flagged case against the required evidence before any action proceeds]**, so that **[governance outcome — e.g. no system action is taken on a low-confidence case without documented human judgement]**.

**Acceptance Criteria**

| Field | Description |
|---|---|
| Given / When / Then | Testable pre-condition, trigger, and expected system + human behaviour |
| Time Window | Maximum time from trigger to required human action |
| Evidence Presented | What information must accompany the escalation (link to Template 3 for detail) |
| Definition of Done | What confirms this story is satisfied at UAT — not "reviewer was notified" but "reviewer could act correctly on what they received" |

### User Story 2

> As a **[role — e.g. compliance officer]**, when **[condition — e.g. an escalation from the first-line reviewer meets the mandatory escalation condition in Template 1, Section D]**, I must **[action — e.g. receive the case with full escalation history and render a documented decision within the required timeframe]**, so that **[governance outcome — e.g. escalations do not stall in an ungoverned queue and the second-line decision is independently attributable]**.

**Acceptance Criteria**

| Field | Description |
|---|---|
| Given / When / Then | Testable pre-condition, trigger, and expected system + human behaviour |
| Time Window | Maximum time from trigger to required human action |
| Evidence Presented | What information must accompany the escalation (link to Template 3 for detail) |
| Definition of Done | What confirms this story is satisfied at UAT |

### User Story 3

> As a **[role — e.g. named out-of-design authority]**, when **[condition — e.g. the system encounters a scenario outside the boundaries defined in Template 1, Section C3]**, I must **[action — e.g. record what was known, what was decided, why, and what evidence existed before authorising any action]**, so that **[governance outcome — e.g. judgement under uncertainty remains distinguishable from undocumented discretion]**.

**Acceptance Criteria**

| Field | Description |
|---|---|
| Given / When / Then | Testable pre-condition, trigger, and expected system + human behaviour |
| Time Window | Maximum time from trigger to required human action |
| Evidence Presented | What information must accompany the escalation (link to Template 3 for detail) |
| Definition of Done | What confirms this story is satisfied at UAT |

*Add rows as required — one story per intervention threshold in Template 1, Section D, plus one for each out-of-design trigger in Section C3.*

## D. Backlog Readiness Sign-Off

| Field | Notes |
|---|---|
| Business Analyst Sign-Off | Confirms every threshold in the linked specification has a corresponding story |
| Product Owner Sign-Off | Confirms stories are prioritised and backlog-ready |
| QA Lead Sign-Off | Confirms every acceptance criterion is independently testable |

---

*Before the System Acts · Template 2 of 3: Escalation Criteria in User Story Format · Raghav Kapoor, CBAP · [linkedin.com/in/raghavkapoor01](https://linkedin.com/in/raghavkapoor01)*
