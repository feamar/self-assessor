# Architecture decision records

This is the **authoritative status index**. Decisions in **Active** govern the current assessment model. **Inactive** holds historical baselines and decisions replaced by later ADRs. No historical file is deleted: superseded records remain accessible with a pointer to their successor. "Retired dimension" inside an **active ADR** means its *removal is still in force*; it does **not** mean that the decision itself is inactive.

## Active

### Metric and dimension simplification

| Original dimension | Current decision | ADR |
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

### Retained exceptions and metric interpretation

| Decision | ADR |
|---|---|
| Keep non-universal D09 and D14 as optional diagnostics | [ADR-0017](0017-retain-non-universal-diagnostics.md) |
| Distinguish outcome-oriented from hard-to-game and define 18 active checks | [ADR-0019](0019-separate-outcome-orientation-from-gameability.md) |

### Governance, reports and agent actions

| Decision | ADR |
|---|---|
| Record every accepted architectural decision in an ADR | [ADR-0018](0018-document-all-architectural-decisions.md) |
| Produce bounded agent improvement skills from justified findings | [ADR-0022](0022-agent-improvement-skills.md) |
| Provide candid criticism, earned praise and precise recognition of excellence | [ADR-0023](0023-candid-evidence-specific-feedback.md) |
| Assess all three perspectives; preserve separate Markdown outcomes and display the selected one | [ADR-0024](0024-all-perspectives-separate-outcomes.md) |
| Active judgment calibration and three-paragraph report policy | [ADR-0025](0025-consolidated-judgment-and-report-policy.md) |

## Inactive — historical or superseded

| ADR | Inactive reason | Superseding current decision |
|---|---|---|
| [ADR-0000](0000-original-assessment-rationale.md) | Historical 30-dimension v1.3 baseline and its reasons; earlier 24 → 25 → 30 lineage. **Inactive**, not a current scoring policy | Current [metric criteria](../../.github/skills/software-delivery-assessment/references/metrics.md) and [active dimension decisions](#metric-and-dimension-simplification) |
| [ADR-0020](0020-calibrated-qualitative-perspectives.md) | Superseded; original one-selected-perspective rule obsolete | [ADR-0025](0025-consolidated-judgment-and-report-policy.md), [ADR-0024](0024-all-perspectives-separate-outcomes.md) |
| [ADR-0021](0021-three-paragraph-report.md) | Superseded; original single-report framing replaced by three independent reports | [ADR-0025](0025-consolidated-judgment-and-report-policy.md) |

**Historical lineage:** 24 documented initial dimensions → 25 after transparency was added → 30 in the expanded pilot → 18 active checks after simplification. The historical ADR-0000 is descriptive, **not a directive to restore old measures**.
