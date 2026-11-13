# Strong metrics and three layers

The active assessment has **18 dimensions: 4 primary outcome metrics, 4 conditional diagnostics/diagnostic questions and 10 essential assurance questions**. Do not call all 18 numerical metrics.

A metric is useful only if it measures a clear result. Define events, unit, period, scope, source, sample size and exclusions; report actual values and trends. **Do not turn missing data into a zero or invent a maturity score.**

## 1. Primary outcomes

| Outcome | Measurement |
|---|---|
| End-to-end lead time | Time from request entering delivery to requested capability available to users; show median and tail where sample permits |
| Deployment frequency | Genuine successful production deliveries per service and period |
| Recovery time | Time from user-impacting failure to restored useful service, on actual recovery events |
| User-facing unavailability | Time users could not complete the service's key activities |
| First-pass acceptance yield (when naturally recorded) | Outcomes independently accepted without corrective rework / assessed outcomes |
| Change-caused user disruption (when attributable) | Observed user impact due to a delivery change; avoid speculative attribution |

The first four are default metrics when applicable. The last two are **conditional candidates**: skip rather than infer acceptance or causation. A period with no failure is **not** evidence of fast recovery.

## 2. Targeted diagnostics

- **D03 — Change failure rate:** failed production changes / relevant changes. Simple **when** change and incident/rollback events are explicitly linked. Otherwise ask what happened to the most recent failed release and label the rate unknown.
- **D09 — Requirement-to-test linkage (non-universal):** linked requirements / relevant requirements. Simple **when** requirements and tests have native, meaningful links. It is a **process proxy**, not an outcome score. Otherwise ask how an important acceptance requirement is verified.
- **D14 — Flaky test feedback (non-universal):** use observed reruns/intermittent outcomes if directly recorded; otherwise inspect recent test reliability evidence.
- **D23 — Time to detect user impact:** use observed incident/monitoring timestamps where trustworthy; otherwise ask how degradation would be noticed.

Do **not** calculate deployment rework rate, mutation score, failure-mode coverage, architecture conformance percentage, security findings hypothetically prevented, vulnerability exposure time, business-impact index, incident recurrence rate or alert actionability rate as default metrics. Do not substitute TDD/BDD adoption, ADR totals, PR size, progressive rollout use or automation percentage as outcome metrics. See [ADRs](../../../../docs/adr/README.md) for rationale.

## 3. Assurance checks

Use focused questions and concrete evidence for test effectiveness, release/rollback safety, integrity, security, privacy, supply chain, access/secrets, relevant non-functional behavior, monitoring and AI controls. See [active checks](dimensions.md). Mark each **effective / concerning / unknown / N/A**, not 0–4.

## Metric strength

| Criterion | Strong when |
|---|---|
| Simple | The result is trivially available from the process, non-convoluted and explainable to a layperson |
| Hard to game | Optimizing the metric cannot be done without improving the result it is intended to represent, regardless of whether the metric concerns a process or outcome |
| Output oriented | Measures an actual result, not whether people follow a prescribed process; **this says nothing by itself about gameability** |
| Universal | Underlying principle applies across domains with possible wording changes |
| Transparent | The measured thing and how to determine its value are unambiguous |

**Universality is preferred for headline outcome metrics, not an absolute requirement for useful specialist diagnostics.** D09 and D14 are explicitly accepted as optional non-universal diagnostics ([ADR-0017](../../../../docs/adr/0017-retain-non-universal-diagnostics.md)).

**Separate the tests.** D09 requirement-to-test linkage is process-oriented (links exist), and may also be gameable (superficial links can raise the percentage): two distinct weaknesses. D14 flakiness measures a testing-process outcome (stable feedback); assess whether that metric can be gamed independently. See [ADR-0019](../../../../docs/adr/0019-separate-outcome-orientation-from-gameability.md).

**Lead time is the 5/5 reference.** Smaller batches and faster deployment are genuine capability improvements, not gaming. Distinguish a badly defined event from a weakness in the intrinsic metric. Data availability is a feasibility question, not metric strength.
