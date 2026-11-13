# Three-layer assessment model

Do not average unlike measures into one maturity score. Report measured values and their trends, then explain causes and verify critical controls. For every metric define **start/end events, scope, unit, numerator/denominator if applicable, observation period, exclusions, source and sample size**. Treat unavailable data as unknown.

## 1. Primary outcomes — delivery capability

| Metric | Intended outcome | Measure |
|---|---|---|
| End-to-end lead time | Respond to demand quickly | Elapsed time from request entering the process to requested capability available to users; report distribution (e.g. median and tail) |
| Deployment frequency | Ability to deliver changes frequently | Real successful production deliveries per service and period, with scope explicitly defined |
| Recovery time | Restore useful operation quickly | Elapsed time from service-impacting failure to restored user-facing operation, on observed events |
| User-facing unavailability | Keep service available | Time or proportion of time users cannot successfully complete key activities |
| First-pass acceptance yield | Deliver what was wanted without rework | Independently accepted outcomes without corrective rework / outcomes assessed |
| Change-caused disruption | Deliver without harming users | User-impacting disruption time or severity attributable to changes, with attribution limits |

Do not assume that an event-free period proves excellent recovery performance. Use context, sample sizes and meaningful definitions, not a universal benchmark. Where a primary metric is inapplicable, say so; retain useful service-specific outcomes.

## 2. Diagnostic metrics — understand performance

Use only as relevant: change failure/rework rates, escaped defects, mutation detection, flaky tests, vulnerability exposure time, time to detect, change size, automation handoffs, and incident recurrence. They explain outcomes; improving a proxy is not itself proof of better delivery.

## 3. Assurance controls — unacceptable risks

Evaluate demonstrated effectiveness of architecture and security rules, privacy/threat review, dependency controls, access/secrets, release safeguards, approvals and AI permissions/independent verification. Evidence of a policy alone is not evidence that it works. Do not average safety obligations into outcome metrics or conceal critical failures.

## Metric strength — assess the metric, not reporting maturity

| Criterion | Strong when |
|---|---|
| Simple | Non-convoluted; the process naturally knows its value and its bottom-line relevance is easy to explain |
| Hard to game | Improving the metric requires improving its intended capability or result |
| Output oriented | Measures an achieved result, not compliance with a prescribed process |
| Universal | The underlying principle works across domains, allowing different terminology |
| Transparent | Exactly what is measured and how to determine the value are clear |

**End-to-end lead time is the 5/5 reference metric.** Do not treat use of smaller changes, quicker automation or higher frequency as gaming when they genuinely improve responsiveness. Misclassified/fabricated events are issues of transparency or data integrity, not automatic evidence that the metric is gameable. Avoid declaring other metrics 5/5 without examining their specific definitions.
