# ADR-0000: Why we started with 30 software delivery dimensions

**Status:** Historical baseline — inactive; this explains the starting point, not today's assessment policy  
**Source:** Software Delivery Assessment Copilot Skill v1.3, original 30-dimension rubric (references/dimensions.md in the v1.3 source archive); earlier 24- and 25-dimension assessment workbooks.

## Context and original objective

We wanted Copilot to assess **the ability to deliver useful software reliably**, using verifiable repository, CI/CD, production, security, test and interview evidence rather than assurances or vendor ratings. The early model was deliberately comprehensive: it tried to expose delivery speed, release quality, specification/test quality, architecture, secure engineering, operations, customer outcomes and AI readiness. Each dimension was included because it seemed to reveal either **a useful result** or **a mechanism that could make the result dependable**. The original rubric proposed observable audit probes and 0–4 maturity anchors, but those anchors were subsequently rejected as a headline composite.

The **30 dimensions** below are the baseline from the expanded v1.3 skill. This is not a claim that all 30 existed in the earliest workbook: the earlier assessment evolved from **24**, to **25** (adding metric publication/transparency), then to **30** (adding incident learning, batch discipline, progressive delivery, automation and monitoring/SRE). The later ADRs explain why some were retired or changed.

## The original 30: purpose of each dimension

| ID | Original dimension | Why it was included |
|---|---|---|
| D01 | Change lead time | Measure delivery speed and expose delays. The original measure was **commit-to-production**; our current stronger definition is **request-to-user-available** lead time. |
| D02 | Deployment frequency | Measure the ability to release changes regularly and respond to demand. |
| D03 | Change fail rate | Keep release speed accountable to production failures and urgent intervention. |
| D04 | Failed deployment recovery | Measure how quickly a service can recover when a release harms users. |
| D05 | Deployment rework rate | Reveal how much delivery effort goes to unexpected corrective releases instead of new intended outcomes. |
| D06 | Metric publication and transparency | Make published performance evidence complete, timely, reproducible and open to scrutiny. |
| D07 | Build and promote once | Establish that the artifact tested and approved is the artifact actually deployed. |
| D08 | Rollback and migration safety | Limit consequences of bad releases, including unsafe data migrations and difficult reversals. |
| D09 | Requirement-to-test traceability | Establish whether essential requested behavior and exceptions have identifiable executable verification. |
| D10 | TDD evidence | Test whether the claimed fail-first practice was actually used, rather than inferring it from test counts. |
| D11 | BDD scenario completeness | Check that important business journeys, alternatives and invalid scenarios were understood and tested. |
| D12 | Test effectiveness | Determine whether tests detect meaningful faults, not merely run code or increase coverage. |
| D13 | Negative, boundary and property tests | Look for defects hidden outside happy paths, at boundaries and in important invariants. |
| D14 | Fast and trustworthy test feedback | Expose slow, intermittent or misleading test feedback that blocks safe frequent delivery. |
| D15 | Non-functional quality checks | Check relevant performance, resilience, accessibility and other quality risks beyond functional behavior. |
| D16 | Architectural conformance | Identify structural drift and violations of architecture constraints that could create future change cost or risks. |
| D17 | Secure coding conformance | Verify security rules affect delivered code and release gates rather than existing only in documents. |
| D18 | Threat and privacy analysis | Detect security and privacy harms early enough for meaningful mitigation. |
| D19 | Dependencies and supply chain | Address known vulnerable dependencies, third-party risk, software provenance and compromised artifacts. |
| D20 | Access, secrets and separation | Limit unsafe privileged change paths, leaked secrets and unauthorized production actions. |
| D21 | Exceptions and ADR audit trail | Make deviations from standards justified, reviewable and auditable rather than invisible. |
| D22 | Service reliability and SLOs | Connect delivery to the reliability users experience and agreed service expectations. |
| D23 | Deployment observability | Make it possible to connect a release to real operational changes and diagnose regressions. |
| D24 | Measured user and business outcomes | Check that shipping work produces actual user or organizational benefit, not merely engineering activity. |
| D25 | AI context, rights and validation | Bound AI permissions and information exposure; independently verify AI-generated contributions. |
| D26 | Incident learning and blameless postmortems | Establish whether real incidents produce verified prevention and operational learning. |
| D27 | Change size and batch discipline | Investigate whether large batches undermine reviewability, flow, reversibility and change safety. |
| D28 | Progressive delivery and rollout strategy | Limit the impact of risky releases with staged exposure, health checks and abort/recovery options. |
| D29 | Delivery automation and manual intervention | Find avoidable handoffs and fragile manual release steps that slow or destabilize delivery. |
| D30 | Operational monitoring, alerting and SRE practice | Ensure user impact can be detected, understood and acted upon; connect observability to real operations. |

## Why this design changed

The original inventory was useful for **discovering risks and candidate evidence**, but it treated dissimilar things as equivalent: actual outcomes (lead time, deployment frequency, recovery), specialist diagnostic measures (test flakiness), implementation choices (TDD, BDD, canaries, automation), and assurance obligations (security, privacy, provenance). A count of compliant processes cannot stand in for proof that delivery is good. Several proposed numerical metrics were also hard to define simply or transparently.

Our later decisions adopted five metric-strength criteria: **simple, hard to game, outcome oriented, universal, transparent**. These are separate criteria; in particular, measuring a result is different from being resistant to gaming. We kept D03 and D09 when their data is naturally available and accepted optional non-universal diagnostics where useful. We eliminated weak metrics, retained consequential risks as questions, and reduced the active inventory to **18 checks** (4 primary outcomes, 4 diagnostics or diagnostic questions and 10 assurance questions).

Finally, the framework stopped averaging scores and instead demands **candid, evidence-calibrated expert judgments** from all three perspectives—conventional, AI-assisted and AI-driven—saved as separate short Markdown outcomes. A credible sustained history matters more than a polished checklist. The historical 30-dimensional baseline is **not** an instruction to restore retired dimensions or a requirement to score every old item.

## Consequences

This ADR preserves **why the 30 dimensions originally seemed useful** without pretending their earlier selection is current policy. It is **inactive history**. The active decisions in the ADR index, the skill and its references define today's assessment; individual dimension-removal ADRs explain subsequent changes. The source rationale is reconstructed from the original metric descriptions and audit probes, not presented as quotations from an undocumented original meeting.
