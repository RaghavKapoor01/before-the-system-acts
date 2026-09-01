# Before the System Acts — Part 2 of 4

## The Upstream Layer — Three Questions That Must Be Answered Before Deployment

Part 1 established that the governance gap is a specification gap. Practitioners across execution architecture, audit, AML compliance, and operational risk independently arrived at the same description of it: the system being governed was never built with specifiable boundaries in the first place.

This part addresses what closes it.

Not a new governance framework. Not a more detailed policy document. Not a better audit trail. The answer is three questions that must be answered in writing, in testable terms, before an AI system is permitted to act with consequence. Until they are, no governance framework can enforce against them and no audit trail can evidence them.

## The Three Questions

Every point at which an AI system acts with consequence requires three things to be written as testable specification artefacts before deployment:

1. **Execution boundary** — the conditions under which the system is permitted to act autonomously.
2. **Intervention threshold** — the conditions under which it must stop and a human must decide.
3. **Evidence standard** — what must exist at that decision point to prove the human could intervene correctly.

These are not governance questions. They are specification requirements. The governance framework describes the intent. These three questions produce the artefacts that make the intent enforceable.

## Why the Intervention Threshold Is the Hardest

In practice, the first and third questions are tractable. The execution boundary can be derived from existing policy — underwriting rules, claims thresholds, credit criteria — the conditions already exist in some form and the work is largely formalisation. The evidence standard is shaped substantially by what regulators already require. MAS FEAT, CBUAE's 2026 guidance, and equivalent frameworks specify categories of evidence examiners expect to see.

The intervention threshold is structurally different. It requires specifying not just when a human should be alerted, but what that human needs to know, how much time they realistically have, and what would count as a correct intervention at the speed the system operates.

Ramya Amballa, a GRC and cyber risk advisor working on CBUAE-aligned AI governance, identified what gets presented to examiners in place of this specification:

> "An override rate without documented intervention criteria is just a number with nothing attached to it."
> — Ramya Amballa, GRC and Cyber Risk Advisor, CBUAE Alignment

Override rates, escalation logs, and training completion records are the most commonly presented evidence of human oversight. Amballa's point is that none of them demonstrate it. A high override rate could mean reviewers are catching errors effectively, or it could mean the system is poorly calibrated and reviewers are guessing. The number alone cannot distinguish between these. What distinguishes them is whether the institution can show, for a specific case, what the reviewer was shown, how long they had to decide, and what the predefined standard for a correct decision was at that moment.

> "A training completion certificate instead of a control that actually fires when something goes wrong."
> — Ramya Amballa, GRC and Cyber Risk Advisor, CBUAE Alignment

Dušica Živanović, working on AI governance and control architecture for high-stakes systems, frames the same requirement as a design principle: the level of autonomy an AI system is granted should be inversely proportional to the cost of an error, and the conditions under which a high-cost decision is permitted to execute must be defined before the system is given the authority to make it.

> "The challenge is not whether an AI system can make a decision. The challenge is whether the organisation has defined the conditions under which that decision is allowed to be made."
> — Dušica Živanović, AI Governance and Control Architecture

The framework described in this article is not a new governance methodology. It is a pre-sign-off checklist for AI requirements work. The three questions are what testable acceptance criteria for human oversight requirements produce when written correctly. Organisations that skip this step do not create a governance gap intentionally. They create it because loosely described requirements pass sign-off without anyone asking whether the human oversight behaviour is specified precisely enough to enforce. By the time an examiner asks, the specification work cannot be retrofitted without significant cost. The checklist exists to prevent that.

## Why This Is a Business Analysis Failure, Not Only a Governance Failure

The same failure shows up in the language of delivery. Business analysts have a quality standard for requirements called INVEST, and the most important criterion is Testable.

An acceptance criterion for a human oversight requirement is commonly written as: *a human reviews high-risk decisions before they are finalised.* This statement cannot be tested — not because the QA analyst lacks skill, but because the upstream specification was never resolved. What counts as high-risk? What must the reviewer see? How long do they have? What constitutes a correct review?

The standard response to an untestable acceptance criterion is to send it back for clarification. In an AI governance context, that response fails. The person who wrote the criterion is not the person who can resolve the ambiguity. The ambiguity originates upstream, in a specification session that should have defined the execution boundary and the intervention threshold before any user story was written.

Until that session happens, no amount of rewriting will make the acceptance criterion testable. It will produce a more detailed version of the same unresolved question.

## The Framework in Delivery

The evidentiary grounding for this framework comes from an AI-enabled claims transformation at a major Asia-Pacific Life and Health insurer operating under MAS regulatory oversight.

The programme introduced AI-assisted processing across health and life insurance claims, using OCR extraction and a confidence-scored rules engine to determine which claims could be processed without human review. The initial design specified a single confidence threshold above which claims proceeded automatically, below which they were routed to a human adjudicator.

**Case Study: Resolving Tiered Thresholds in Health & Life Insurance.** A single threshold could not distinguish between two structurally different causes of low confidence: poor document scan quality, which had no bearing on claim legitimacy, and genuine claim complexity, which did. The correction was a tiered threshold architecture that separated these two variance sources and defined distinct execution boundaries and escalation criteria for each.

This addressed the execution boundary. It did not, on its own, address the intervention threshold. The adjudicators receiving escalated claims still needed a specification of what information they required, at what point a claim became time-sensitive, and what would constitute a correct override decision under MAS regulatory expectations. That specification was built alongside the threshold redesign, which reduced false escalations by 40 percent while maintaining the evidence trail required for regulatory examination.

The lesson from that delivery is the framework this series describes. The execution boundary alone is not enough. The intervention threshold must be specified with equal precision. And the evidence standard must be defined before deployment, not reconstructed after an incident makes its absence visible.

## The Question That Follows

Part 1 asked where AI governance actually fails. Part 2 has described what closes the gap at the point where it can still be closed. Before the system acts.

Part 3 addresses what happens after the specification exists: how an organisation validates, in production, that the boundaries it specified are holding — and why the monitoring layer, however sophisticated, cannot substitute for the upstream specification work this part describes.

---

*Follow the complete series: #BeforeTheSystemActs*

*Part 1: The Gap — Why upstream specification is the missing prerequisite in AI governance*
*Part 2: The Upstream Layer — Three questions that must be answered before deployment*
*Part 3: The Downstream Layer — What production validation requires, and what it cannot*
*Part 4: The Regulatory Context — UAE, CBUAE, and what the September 2026 deadline requires*

*Before the System Acts is a practitioner framework on AI governance specification in regulated financial services.*
