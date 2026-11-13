# Assessment simplification decisions

These are **architecture decision records**, not agent instructions. They document why dimensions from the initial 30-dimension inventory were removed or reframed, avoiding unnecessary process metrics.

- **Retired**: no longer a standalone assessment dimension.
- **Reframed**: metric discarded; consequential concern remains as an evidence question.

| Original ID | Decision | ADR |
|---|---|---|
| D05 | Retired | [0001-d05-deployment-rework-rate.md](0001-d05-deployment-rework-rate.md) |
| D06 | Retired | [0002-d06-metric-publication-and-transparency.md](0002-d06-metric-publication-and-transparency.md) |
| D10 | Retired | [0003-d10-tdd-evidence.md](0003-d10-tdd-evidence.md) |
| D11 | Retired | [0004-d11-bdd-scenario-completeness.md](0004-d11-bdd-scenario-completeness.md) |
| D12 | Reframed | [0005-d12-test-effectiveness.md](0005-d12-test-effectiveness.md) |
| D13 | Retired | [0006-d13-negative-boundary-and-property-tests.md](0006-d13-negative-boundary-and-property-tests.md) |
| D16 | Retired | [0007-d16-architectural-conformance.md](0007-d16-architectural-conformance.md) |
| D17 | Reframed | [0008-d17-secure-coding-conformance.md](0008-d17-secure-coding-conformance.md) |
| D19 | Reframed | [0009-d19-dependencies-and-supply-chain.md](0009-d19-dependencies-and-supply-chain.md) |
| D21 | Retired | [0010-d21-exceptions-and-adr-audit-trail.md](0010-d21-exceptions-and-adr-audit-trail.md) |
| D24 | Retired | [0011-d24-measured-user-business-outcomes.md](0011-d24-measured-user-business-outcomes.md) |
| D26 | Retired | [0012-d26-incident-learning-and-postmortems.md](0012-d26-incident-learning-and-postmortems.md) |
| D27 | Retired | [0013-d27-change-size-and-batch-discipline.md](0013-d27-change-size-and-batch-discipline.md) |
| D28 | Retired | [0014-d28-progressive-rollout-strategy.md](0014-d28-progressive-rollout-strategy.md) |
| D29 | Retired | [0015-d29-delivery-automation-and-manual-intervention.md](0015-d29-delivery-automation-and-manual-intervention.md) |
| D30 | Reframed | [0016-d30-operational-monitoring-alerting-and-sre-practice.md](0016-d30-operational-monitoring-alerting-and-sre-practice.md) |

## Retained specialist-metric exceptions

| IDs | Decision | ADR |
|---|---|---|
| D09, D14 | Retained as optional non-universal diagnostics | [ADR-0017](0017-retain-non-universal-diagnostics.md) |

D03 remains a conditional diagnostic: its measurement is straightforward where the environment maintains reliable linked events; otherwise ask a focused question or report unknown.

## Repository governance

| Decision | ADR |
|---|---|
| Record every accepted architectural decision alongside the change | [ADR-0018](0018-document-all-architectural-decisions.md) |

## Metric-strength interpretation

| Decision | ADR |
|---|---|
| Distinguish outcome orientation from hard-to-game; name the 18 dimensions correctly | [ADR-0019](0019-separate-outcome-orientation-from-gameability.md) |

## Perspective judgments, reports and agent actions

| Decision | ADR |
|---|---|
| Replace weighted scores with calibrated qualitative perspective judgments | [ADR-0020](0020-calibrated-qualitative-perspectives.md) |
| Limit executive assessment to three paragraphs | [ADR-0021](0021-three-paragraph-report.md) |
| Draft independent agent skills for justified improvements | [ADR-0022](0022-agent-improvement-skills.md) |

## Feedback and outcome artifacts

| Decision | ADR |
|---|---|
| Give candid evidence-specific criticism, earned praise and exact reasons for excellence | [ADR-0023](0023-candid-evidence-specific-feedback.md) |
| Always evaluate all three perspectives, store separate Markdown outcomes and show the user's selection | [ADR-0024](0024-all-perspectives-separate-outcomes.md) |
