# Scoring Model Guide

## Design goals

The model is designed to be:

- Explainable: every score has a visible criterion, scale, and weight.
- Auditable: assumptions, missing data, and decision changes can be logged.
- Flexible: categories and weights can be calibrated by portfolio type.
- Conservative: mandatory work is flagged rather than hidden inside discretionary ranking.
- Practical: non-specialists can use it without advanced optimization tooling.

## Default formula

```
Normalized Score = (sum(score_i * weight_i) / 5) * 100
```

Where:

- Each criterion score is on a 1-5 scale.
- Each criterion weight is a decimal.
- Active weights must sum to 1.00.
- The final score is expressed on a 0-100 scale.

## Default criteria

| Criterion | Default weight | Plain-language meaning |
| --- | ---: | --- |
| Strategic alignment | 25% | How directly the initiative supports declared strategy. |
| Financial or mission value | 15% | Expected revenue, savings, cost avoidance, mission value, or measurable enterprise benefit. |
| Customer or operational impact | 15% | Degree of customer, employee, operating, service, or process impact. |
| Risk reduction or compliance criticality | 15% | Value of reducing legal, regulatory, security, operational, or business risk. |
| Dependency enablement | 10% | Degree to which the initiative unlocks or protects other important work. |
| Readiness and confidence | 10% | Confidence in scope, sponsorship, estimates, solution approach, and execution readiness. |
| Effort or cost feasibility | 10% | Affordability and execution burden, scored higher when effort is more feasible. |

## Scale anchors

Use a 1-5 scale.

| Score | Meaning |
| ---: | --- |
| 1 | Weak, low, unclear, poor fit, or unsupported. |
| 2 | Limited value or weak evidence. |
| 3 | Moderate value, acceptable evidence, or normal fit. |
| 4 | Strong value, clear evidence, or high fit. |
| 5 | Critical, exceptional, mandatory, or top-tier evidence. |

## Value-evidence confidence anchors

When scoring financial, mission, risk, customer, or operational value, attach a
value-evidence label. Do not let a high value narrative outrank evidence quality
without a visible caveat.

| Label | Meaning | Scoring treatment |
| --- | --- | --- |
| Measured value | Baseline, target, source, owner, and actual or validated current evidence are available. | Can support high value score if other criteria also support it. |
| Directional value | Baseline or target is plausible and source/owner are known, but actuals or validation are still maturing. | Can support moderate to strong score with confidence caveat. |
| Proxy value | Uses indirect measure, qualitative signal, or partial evidence. | Keep score conservative and route measurement gap downstream. |
| Unsupported value | Claim lacks baseline, source, owner, validation, or clear metric. | Do not use as primary basis for high score; flag for intake cleanup or value-ledger follow-up. |

If the value score is 4 or 5 while evidence is proxy or unsupported, call out the
tension in the summary and decision brief. Mandatory work remains separate from
discretionary ranking; mandatory status does not prove benefit realization.

## Calibration rules

1. Avoid criteria overlap. If strategic alignment and financial value always move together, clarify the difference.
2. Keep the model to 5-8 criteria. More criteria usually creates false precision.
3. Make weights visible and approved by the portfolio board.
4. Use mandatory classification as a portfolio constraint, not just a scoring boost.
5. Use readiness and confidence to prevent weak business cases from ranking too high.
6. Keep cost or effort visible separately even when effort feasibility is scored.
7. Recalibrate quarterly or when strategy changes materially.

## Treatment of mandatory work

Mandatory work should be categorized before discretionary ranking:

- Legal or regulatory requirement
- Safety or security commitment
- Contractual obligation
- Audit finding or remediation commitment
- Executive-committed work already funded or externally promised

Mandatory work can still be scored to understand burden and sequencing, but the brief should separate mandatory commitments from discretionary trade-offs.

## Common anti-patterns

| Anti-pattern | Why it fails | Correction |
| --- | --- | --- |
| Ranking everything in one list | Mandatory and discretionary work get mixed together. | Separate commitments, discretionary choices, and governance holds. |
| Too many criteria | Creates false precision and slows adoption. | Use fewer criteria with clear scale anchors. |
| Unweighted votes | Treats every factor as equally important. | Confirm and document weights. |
| Hidden math | Stakeholders cannot challenge the output. | Show the formula, weights, and score drivers. |
| No confidence flag | Weak data looks as strong as validated data. | Add evidence and confidence ratings. |
| Value story outruns evidence | A compelling business narrative receives a high score without baseline/source/owner support. | Add value-evidence labels and route unsupported claims to cleanup or value follow-up. |
| Missing decision rights | Scores exist but nobody owns the decision. | Identify sponsor, owner, and decision authority. |
