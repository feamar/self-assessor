# Dimension rubric

Assess one service over an explicit period. For every dimension use **0** demonstrably absent/ineffective, **1** ad hoc/manual, **2** repeatable but partial, **3** enforced and evidenced across meaningful scope, **4** measured over time, independently challenged and improved. Apply these anchors to the dimension-specific behavior below; an assertion of practice alone is not evidence of enforcement. **Unknown** is not 0; **N/A** requires a rationale.

| ID | Dimension | Inspect / test for |
|---|---|---|
| D01 | Change lead time | Linked change-to-production timestamps, distribution, trends and bottlenecks |
| D02 | Deployment frequency | Successful production deployment events per service and period |
| D03 | Change fail rate | Changes causing incidents, rollback or remediation; explicit denominator |
| D04 | Failed deployment recovery | Recovery events, elapsed times and actual restoration |
| D05 | Deployment rework rate | Unplanned fixes/rework following releases, with linked evidence |
| D06 | Metric publication and transparency **(critical)** | Published, reproducible delivery measures and definitions; score 0 if demonstrated absent, without inventing underlying metrics |
| D07 | Build and promote once | Immutable artifacts, provenance and environment promotion, not rebuild-per-stage |
| D08 | Rollback and migration safety **(critical)** | Exercised rollback, data migration compatibility and recovery |
| D09 | Requirement-to-test traceability | Critical requirements mapped to meaningful executable checks |
| D10 | TDD evidence | Observable red-to-green chronology, not just presence of tests |
| D11 | BDD scenario completeness | Business examples, negative/exception cases and maintained acceptance checks |
| D12 | Test effectiveness **(critical)** | Assertions/oracles, seeded-fault or mutation detection, defects caught |
| D13 | Negative, boundary and property tests | Failure paths, edge cases, invariants and representative adversarial inputs |
| D14 | Fast, trustworthy test feedback | Execution times, flakiness, quarantine and failure handling |
| D15 | Non-functional quality checks | Performance, resilience, accessibility and security checks relevant to risks |
| D16 | Architectural conformance | Versioned architectural rules, dependencies, exceptions and verified enforcement |
| D17 | Secure coding conformance **(critical)** | Applicable approved rules, actual findings, enforcement and exception handling |
| D18 | Threat and privacy analysis **(critical)** | Risk-driven threat/privacy review, mitigations and review cadence |
| D19 | Dependencies and supply chain **(critical)** | Dependency scanning, provenance/SBOM where relevant, patch and license decisions |
| D20 | Access, secrets and separation **(critical)** | Least privilege, protected secrets, approvals and separation of duties |
| D21 | Exceptions and ADR audit trail | Recorded decisions, deviations, rationale, approvals and follow-up |
| D22 | Service reliability and SLOs | Defined user-facing objectives, observed service levels and error-budget decisions |
| D23 | Deployment observability | Version/change correlation, logs, traces, metrics and release verification |
| D24 | Measured user/business outcomes | User outcomes and operational impacts linked to changes |
| D25 | AI context, rights and validation **(critical if AI used)** | Approved model/context, scoped permissions, independent verification and traceability |
| D26 | Incident learning and postmortems | Real incidents, blameless analysis, tracked actions and recurrence checks |
| D27 | Change size and batch discipline | PR/change distributions, reviewability, WIP and rework |
| D28 | Progressive rollout strategy | Canary/flags/phased rollout, automated health checks and abort evidence |
| D29 | Delivery automation and manual intervention | Actual automated transitions, human toil, failure paths and approvals |
| D30 | Operational monitoring, alerting and SRE practice | Actionable alerts, ownership, on-call response, runbooks and alert quality |

## Dimension-specific interpretation

- For **D01–D05**, do not impose universal "good" DORA thresholds. Show observed counts, percentiles and service context; configuration is not measurement.
- For **D09–D15**, inspect test bodies and critical requirements, not just names, counts or coverage percentage. A high coverage number does not prove correctness.
- For **D16–D21**, verify applicable organizational standards before asserting compliance. A policy file proves a rule exists, not that it is enforced. Flag bypassable critical gates.
- For **D22–D24 and D26–D30**, require historical incident, deployment and monitoring evidence for high scores. One interview about the last failed release is a useful probe, not proof of a trend.
- For **D25**, evaluate AI permission boundaries and independent controls, not adoption as an end in itself. Use N/A when no AI is used.
- Record **score, status (verified/provisional/unknown/N/A), evidence IDs, confidence and one-line rationale** per dimension. If a control is genuinely inapplicable, explain why rather than silently excluding it.
