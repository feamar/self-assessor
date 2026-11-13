# ADR-000: Why the original assessment dimensions were selected

**Status:** Historical baseline — inactive as a current assessment policy  
**Original source:** `software_delivery_quality_matrix.xlsx`, first documented assessment workbook (12 November 2026), `Overview` and `Assessment Matrix` sheets.

## Context and provenance

The original aim was an **externally observable software delivery and release-quality assessment**: examine actual evidence rather than accept a team's self-description. We wanted to compare what strong human-led delivery, AI-integrated delivery, and a feasible baseline could look like, then assess one service with a reproducible audit. The starting concerns were DORA-style delivery performance, specification and test rigor (including TDD, BDD and demonstrable defect detection), secure-coding and architectural rules, release assurance and operational reliability. Each proposed dimension needed an observable audit probe, even where it was not a strong outcome metric.

**Historical accuracy:** The request to document the "original 20 metrics" does not match the earliest recoverable artifact. That workbook already has **24 dimensions**, not 20. There is no verified earlier 20-dimension decision list. The following table records the **first 20 rows of that documented 24-dimension matrix** and reconstructs their purpose from the original observable-audit descriptions. This is **not a claim that those 20 once formed a separately approved framework**. The last four rows, documented at the same time, are described below. The original row numbers below are **positions**, not current D-identifiers (later additions changed the numbering).

## The first 20 documented dimensions and why they seemed worth assessing

| Original row | Dimension | Original reason for including it |
|---|---|---|
| 1 | Change lead time | Show how quickly code changes can reach production; expose delays in delivery flow. **Originally commit-to-production**, not today's end-to-end request lead time. |
| 2 | Deployment frequency | Show how often a service can deliver production changes and thus respond to demand. |
| 3 | Change fail rate | Pair delivery speed with the real cost of changes that harm production. |
| 4 | Failed deployment recovery | Measure how quickly useful service is restored after a harmful release. |
| 5 | Deployment rework rate | Expose capacity spent correcting releases instead of delivering intended changes. |
| 6 | Build and promote once | Check that the tested, approved artifact is actually what reaches production. |
| 7 | Rollback and migration safety | Check whether risky changes, including schema changes, can be recovered safely. |
| 8 | Requirement-to-test traceability | Look for evidence that critical requirements and exception paths have executable verification. |
| 9 | TDD evidence | Look for a disciplined testing-before-implementation practice rather than just test counts. |
| 10 | BDD scenario completeness | Look for business behavior and negative/exception scenarios specified and exercised. |
| 11 | Test effectiveness | Ask whether tests actually catch meaningful defects, not merely execute code or inflate coverage. |
| 12 | Negative, boundary and property tests | Seek evidence that verification probes unintended behavior and edge conditions. |
| 13 | Fast and trustworthy test feedback | Identify slow or flaky test feedback that undermines confident delivery. |
| 14 | Non-functional quality checks | Check that relevant performance, resilience and accessibility risks are exercised. |
| 15 | Architectural conformance | Check whether changes respect approved enterprise architecture and known constraints. |
| 16 | Secure coding conformance | Look beyond policy documents to enforced checks and unresolved security findings. |
| 17 | Threat and privacy analysis | Identify security/privacy risks from meaningful changes before they reach users. |
| 18 | Dependencies and supply chain | Look for known-vulnerable dependencies and traceable software/artifact provenance. |
| 19 | Access, secrets and separation | Verify that credentials, privileges and production change paths are controlled. |
| 20 | Exceptions and ADR audit trail | Make architectural/security deviations explainable and accountable during audits. |

## Four more dimensions already in the earliest workbook

| Original row | Dimension | Why it was included |
|---|---|---|
| 21 | Service reliability and SLOs | Tie delivery work to actual user-facing service reliability and incident impact. |
| 22 | Deployment observability | Correlate deployed changes with telemetry so harmful effects are discoverable. |
| 23 | Measured user and business outcomes | Check whether releases produced value rather than just completed engineering activity. |
| 24 | AI context, rights and validation | Examine whether AI works within approved policy, permissions and independent verification. |

The first documented version therefore had **24 dimensions**. A later workbook added **metric publication and transparency**, producing **25**; additional CI/SRE dimensions expanded the pilot skill to **30**. The subsequent simplification deliberately eliminated many method-adoption percentages, opaque composite scores and ambiguous measures. See the later ADRs for individual removals and replacements.

## Why this starting point was reasonable—and why we changed it

The original matrix tried to balance **delivery throughput, change safety, specification/test rigor, architectural/security assurance, operations and AI governance** in one externally auditable framework. That breadth was useful for exploring what evidence existed, but it mixed measured outcomes with **process adherence**, specialist controls and subjective maturity ratings. It also used **commit-to-production** as lead time rather than the stronger end-to-end demand-to-user outcome.

The current policy now favors strong simple/outcome-oriented measurements, targeted diagnostics, critical assurance questions and **three candid, separate qualitative perspective judgments**, not a weighted average of all historical dimensions. The historical reasons above **explain why we started there; they do not restore retired metrics**.

## Consequences

Preserve this ADR as a **historical, inactive baseline** and retain later superseding decisions in the log. Do not infer that a separately approved original set of exactly 20 existed. The working skill and **Active ADRs** govern current assessments.
