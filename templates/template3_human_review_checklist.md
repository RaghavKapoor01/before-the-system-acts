# Template 3 of 3 — Human Review Acceptance Checklist

*Before the System Acts — Practitioner Framework for AI Governance Specification in Regulated Financial Services*

UAT-ready acceptance criteria for the human oversight control defined in the Decision Boundary Specification (Template 1, Section E) and built out as backlog items in Template 2. This checklist is what a QA tester executes to confirm the control is real, not documented theatre.

> **Purpose of this template:** This document is completed by the Business Analyst in partnership with QA before UAT begins. It answers one question precisely: for a given human review point, what must be true for that review to constitute meaningful oversight rather than a formality? Each row is a pass/fail condition — not a principle, not a training objective. If a row cannot be tested by a QA tester without interpretation, it is not ready for this checklist.

## A. Document Control

| Field | Notes |
|---|---|
| System / Initiative Name | Must match the linked Decision Boundary Specification and Escalation Criteria |
| Linked Specification | Version and date of the Template 1 document this checklist is derived from |
| Linked User Story | Which Template 2 story this checklist validates |
| Review Point Name | The specific decision point this checklist governs — one checklist per review point |
| Business Analyst | Named author |
| QA Lead Sign-Off | Confirms every item is independently testable |

## B. Information Sufficiency

*What the reviewer must have in front of them for the review to be possible at all.*

| ✓ | Requirement | Specification (completed by BA) |
|---|---|---|
| ☐ | **Required information items are named explicitly** — not "relevant context"; list every specific data point, score, or document the reviewer must see | |
| ☐ | **Information excludes what the AI generated as unverifiable justification** — the reviewer must be able to check the decision against something the system did not produce | |
| ☐ | **Confidence score or model output is shown alongside, not instead of, underlying evidence** — a score alone is not sufficient information for a meaningful review | |
| ☐ | **Prior/related cases or precedent are accessible if relevant to the decision** — state whether this review point requires historical context, and if so, how it is surfaced | |

## C. Format Sufficiency

*Whether the information is presented in a form a reviewer can actually use under real conditions, not just technically available.*

| ✓ | Requirement | Specification (completed by BA) |
|---|---|---|
| ☐ | **Information is presented in structured form, not raw system logs** — state the actual format: summary screen, structured fields, comparison view, etc. | |
| ☐ | **Format has been tested with an actual reviewer, not only designed by the BA/dev team** — untested formats routinely fail under real review volume and time pressure | |
| ☐ | **Format distinguishes what the system is confident about from what it is uncertain about** — a format that presents everything with equal visual weight defeats the purpose of flagging | |

## D. Time Window

*Whether the reviewer has enough time to exercise judgement, not just enough time to click a button.*

| ✓ | Requirement | Specification (completed by BA) |
|---|---|---|
| ☐ | **Maximum and minimum time windows are both defined** — a review completed in nine seconds is itself a red flag the system should be able to detect | |
| ☐ | **Time window accounts for realistic reviewer caseload, not a single-case pilot assumption** — state the assumed concurrent case volume this time window was calibrated against | |
| ☐ | **Defined consequence exists if the time window is breached** — escalation, system pause, or supervisor notification; a review point with no consequence for lateness is not enforced | |

## E. Decision Criteria and Sufficiency Standard

*What actually distinguishes a meaningful review from a rubber stamp, in terms a QA tester can check.*

| ✓ | Requirement | Specification (completed by BA) |
|---|---|---|
| ☐ | **Reviewer is required to document what they verified, not only their conclusion** — "Approved" is not evidence of review; what was checked, and against what, is | |
| ☐ | **At least one required action forces engagement with evidence the AI did not generate** — this is the anti-automation-bias control; without it, review defaults to confirming the AI's own output | |
| ☐ | **Named conditions exist under which the reviewer must escalate regardless of confidence score** — high confidence does not exempt a case from the conditions defined in Template 1, Section D | |
| ☐ | **A minimum-quality bar for the review itself is defined and auditable** — state what a QA tester or auditor checks after the fact to determine the review was substantive, not just completed | |

## F. Documentation Requirement

*What the review produces, and where it lives, so it is auditable later — not just completed now.*

| ✓ | Requirement | Specification (completed by BA) |
|---|---|---|
| ☐ | **Reviewer's documented reasoning is stored and retrievable by case reference** — state the system of record | |
| ☐ | **Record includes what was verified, the decision, and the reviewer's identity and timestamp** — minimum fields required for audit traceability | |
| ☐ | **Retention period matches the applicable regulatory requirement for this decision type** — confirm with compliance; retention periods vary by jurisdiction and decision category | |

## G. UAT Sign-Off

| Field | Notes |
|---|---|
| QA Lead Sign-Off | Confirms every row above was tested against a real or realistic scenario, not just reviewed on paper |
| Business Analyst Sign-Off | Confirms this checklist reflects the intervention threshold and evidence standard in the linked specification |
| Reviewer (End-User) Sign-Off | Confirms the format and time window are workable under real caseload — not signed off by the BA or QA alone |

---

*Before the System Acts · Template 3 of 3: Human Review Acceptance Checklist · Raghav Kapoor, CBAP · [linkedin.com/in/raghavkapoor01](https://linkedin.com/in/raghavkapoor01)*
