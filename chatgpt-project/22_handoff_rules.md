# Handoff Rules

Portfolio scoring produces decision support, not final decisions. Use handoffs
to move the right outputs into sequencing, governance, value tracking, or
executive review.

## Handoff note format

Source module: Portfolio Prioritization Scoring Agent
Recommended next module or human owner:
Work item:
Lifecycle stage:

Confirmed facts:
Assumptions:
Evidence gaps:
Decisions needed:
Risks, dependencies, or actions:
Value-evidence confidence:
Measurement contract, if value is claimed:
Do not pass downstream:
Suggested first prompt:

## Common handoffs

| Condition | Handoff target | Pass downstream |
|---|---|---|
| Ranking exposes capacity conflict, dependency conflict, or fixed-window tradeoff | Portfolio Capacity Sequencing Planner | Ranked candidates, mandatory work, capacity estimates, dependencies, fixed dates, constraints, decision options |
| Governance forum decisions or follow-up actions are needed | PMO Governance Operations Log | Decision candidates, action items, owners, due dates, rationale, unresolved assumptions, value follow-up actions if measurement gaps affect governance |
| Executive discussion or sponsor tradeoff is needed | Executive Portfolio Review Pack Builder | Portfolio summary, scoring model, options, tradeoffs, risks, missing data, measurement readiness, decisions requested |
| Benefit claims need later measurement | Value Realization Governance Ledger | Value-evidence label, value score tension, measurement contract: expected outcome, benefit type, metric, baseline, target, actual if available, measurement period, source, measure owner, review cadence, validation need, confidence, realization risk, finance-sensitive flag, downstream route |
| Readiness or sponsor data is too weak to score fairly | Portfolio Intake Readiness Triage System or Portfolio Signal Quality Auditor | Missing fields, weak sponsors, unclear decision rights, stale data, duplicate demand, cleanup needs |
| Control or exposure item drives priority | Controls Exposure Governance Toolkit | Risk/control rationale, impacted initiative, evidence, owner, open risk-acceptance questions |

## Do not pass downstream

- Scores as if they are final approval.
- Low-confidence ranks without caveats.
- Hidden weighting assumptions.
- Missing sponsor, owner, decision authority, cost, capacity, or benefit data as if complete.
- Delivery completion or score rank as if it proves value realization.
- High value scores with proxy or unsupported evidence unless the confidence caveat travels with the handoff.
- Sensitive financial or private source detail not needed for the receiving workflow.

## First-prompt examples

Sequencing: "Use this portfolio scoring handoff to build sequencing scenarios. Preserve mandatory work, capacity constraints, dependencies, fixed windows, and unresolved decisions."

Executive review: "Use this scoring summary to build an executive portfolio review section. Show options, tradeoffs, assumptions, and decisions required; do not present scores as final decisions."

Value ledger: "Use this scoring handoff to create or update value-ledger rows. Preserve confidence, realization risk, finance-sensitive flags, and measurement gaps; do not treat portfolio rank as realized value."
