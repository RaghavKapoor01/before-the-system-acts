# Template 1 of 3 — Decision Boundary Specification

*Before the System Acts — Practitioner Framework for AI Governance Specification in Regulated Financial Services*

A pre-deployment specification document defining the conditions under which an AI system is authorised to act, the risk profile of each permitted action across five categories, the actions it is explicitly prohibited from taking, and the conditions that require human authorisation before the system proceeds.

> **Purpose of this template:** This document is completed by the Business Analyst in partnership with the risk owner and business decision authority before an AI system is deployed. It becomes the institutional record of what the system was authorised to do, the risk profile of each permitted action, and the revalidation triggers that connect the specification layer to the production monitoring layer. This is not a policy document. It is a testable specification — written in terms precise enough that a reviewer can determine, at the point of audit, whether any given system action was authorised under the conditions that existed at deployment. Medium and High risk-rated actions feed directly into the monitoring layer's revalidation schedule.

## A. Document Control

| Field | Notes |
|---|---|
| System / Initiative Name | The name of the AI system this specification governs |
| Version | Update on every material change |
| Date of Specification | Date this version was completed and signed off |
| Business Owner | Named individual accountable for the system's business outcomes |
| Risk Owner | Named CRO/CCO or delegate who validated the boundaries in this document |
| Business Analyst | Named BA who authored this specification |
| Review Date | Date by which this specification must be re-validated against current operating conditions |

## B. System Description

| Field | Notes |
|---|---|
| System Purpose | What business problem does this system address? What outcome is it designed to produce? |
| Decision Type | What category of decision does this system influence or make? |
| Operating Environment | Channels, products, customer segments, or jurisdictions affected |
| Regulatory Context | Which regulatory obligations apply to decisions made or influenced by this system? |

## C. Execution Boundary

*Define the precise conditions under which this system is authorised to act. Rate each permitted action across five risk categories. Medium and High ratings feed directly into the monitoring layer's revalidation schedule.*

### C1. Permitted Actions — Risk-Rated Classification

| Risk Category | Financial | Legal / Regulatory | Reputational | Operational | Customer / Third Party | Revalidation Trigger |
|---|---|---|---|---|---|---|
| **Permitted Action 1** *(describe action)* | Low / Medium / High | Low / Medium / High | Low / Medium / High | Low / Medium / High | Low / Medium / High | |
| **Permitted Action 2** *(describe action)* | Low / Medium / High | Low / Medium / High | Low / Medium / High | Low / Medium / High | Low / Medium / High | |
| **Permitted Action 3** *(describe action)* | Low / Medium / High | Low / Medium / High | Low / Medium / High | Low / Medium / High | Low / Medium / High | |
| *Add rows as required — one row per permitted action category* | | | | | | |

**Rating guide:** Low: Standard monitoring, scheduled revalidation only. Medium: Enhanced monitoring, drift-triggered revalidation. High: Continuous monitoring, immediate revalidation on any deviation. Human confirmation required.

| Field | Notes |
|---|---|
| Additional Controls — Medium Risk Actions | For each action rated Medium in any risk category: what additional monitoring, approval, or documentation requirements apply? |
| Additional Controls — High Risk Actions | For each action rated High in any risk category: what enhanced monitoring, mandatory human confirmation, or escalation requirements apply before the system acts? |
| Confidence Threshold | What minimum model confidence score is required for autonomous action in each permitted action category? |

### C2. Prohibited Actions — What the system is EXPLICITLY NOT authorised to do

> ⚠ **Note:** "Not listed above" is not sufficient. Prohibited actions must be named explicitly. This section directly addresses the agentic AI risk: a system given an objective and an open field will use any method available unless prohibited actions are named.

| Field | Notes |
|---|---|
| Prohibited Actions | List every action this system is explicitly prohibited from taking, regardless of how it interprets its objective or what methods it identifies as available |
| Prohibited Data Access | What data sources, systems, or external resources is this system explicitly prohibited from accessing? |
| Prohibited Methods | What methods, pathways, or techniques is this system prohibited from using to achieve its objective? (e.g. exploiting system vulnerabilities, accessing data outside designated scope, interacting with external systems not in its permitted environment) |

### C3. Out-of-Design Protocol — When Reality Falls Outside the Specification

*The specification cannot anticipate every scenario. This section defines the governance protocol for scenarios that fall outside the pre-defined action space — ensuring that accountable judgement under uncertainty is distinguishable from ungoverned discretion.*

| Field | Notes |
|---|---|
| Out-of-Design Trigger | What conditions indicate that a scenario has fallen outside the pre-defined specification boundary? How does the system or reviewer identify that the design does not cover the current situation? |
| Named Out-of-Design Authority | Who has the pre-assigned authority to make a judgement call when the scenario falls outside the design? This must be a named role, not "whoever is available." The authority to act does not require certainty — it requires accountability. |
| Known Scenario Response — Documentation Required | When a known scenario is encountered and the specification is followed: what documentation confirms that the pre-defined threshold, authority, and evidence standard were applied? |
| Unknown Scenario Response — Documentation Required | When a scenario falls outside the design and the named authority exercises judgement: what must be recorded? Minimum: (1) what was known at the time of the decision, (2) what was decided, (3) why, (4) what evidence existed. This record is the boundary between accountable judgement and post-hoc rationalisation. |
| Post-Incident Specification Update | After an out-of-design scenario is resolved: what process determines whether the specification should be updated to cover the newly encountered scenario? Who owns this decision and within what timeframe? |
| Isolation Test | At audit, how will the examiner determine whether any given incident was (a) within design and governed by the specification, or (b) outside design and governed by the out-of-design protocol? The boundary between known and unknown must be auditable. |

**Design Principle:** The specification isolates the known from the unknown. Known scenarios are governed deterministically by sections C1, C2, D, and E. Unknown scenarios are governed accountably by this section. The boundary between them must be visible and auditable.

## D. Intervention Threshold

*Define the precise conditions that require human authorisation before the system proceeds. These are not monitoring triggers — they are the conditions that must stop autonomous execution.*

| Field | Notes |
|---|---|
| Mandatory Human Review Conditions | List every condition requiring human review before the system proceeds. Use measurable criteria, not principles. |
| Mandatory Escalation Conditions | Conditions requiring escalation beyond the first-line reviewer — to a senior authority, compliance, or risk function |
| System Pause Conditions | Under what conditions must the system cease autonomous action entirely, pending investigation or re-authorisation? |
| Override Authority | Who has authority to override a human review decision? What conditions apply? How must an override be documented? |

## E. Evidence Standard

*Define what information the human reviewer must have access to, in what form, and within what timeframe, for a review to constitute meaningful oversight rather than a formality.*

| Field | Notes |
|---|---|
| Required Information at Review Point | What specific information must be presented to the human reviewer? List each required item. |
| Required Format | In what form must information be presented? (e.g. structured summary, raw model output, confidence breakdown) |
| Required Timeframe | Within what timeframe must the reviewer act? What happens if the timeframe is not met? |
| Sufficiency Standard | What constitutes a sufficient review? How will the organisation determine, at audit, whether the review was meaningful? |
| Documentation Requirement | What must the reviewer record? Where is this record maintained? |

## F. Sign-Off and Version Control

*This specification is not effective until signed by all named parties. Any material change to sections C, D, or E requires re-sign-off before the system continues operating.*

| Field | Notes |
|---|---|
| Business Owner Sign-Off | Name / Role / Date / Signature |
| Risk Owner Sign-Off | Name / Role / Date / Signature |
| Compliance Sign-Off (if required) | Name / Role / Date / Signature |
| Version History | Record all versions, dates, and the reason for each update |

---

*Before the System Acts · Template 1 of 3: Decision Boundary Specification · Raghav Kapoor, CBAP · [linkedin.com/in/raghavkapoor01](https://linkedin.com/in/raghavkapoor01)*
