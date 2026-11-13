# ADR-0033: Verify and recommend a trustworthy outcome/DORA metrics dashboard

**Status:** Accepted — active  
**Extends:** [ADR-0028](0028-evidence-first-report-before-optional-agent-skills.md), [ADR-0031](0031-openshift-sync-and-open-ended-evidence.md).

## Context

The assessment test did not strongly recommend an outcomes dashboard, even though the developer could not identify DORA or comparable delivery measurements. Without credible historical outcome measurements, a team cannot readily demonstrate success, track improvements or calibrate the AI-driven perspective.

## Decision

During evidence gathering, **actively search for and ask about existing delivery/outcome/DORA dashboards or recurring evidence reports**. Verify data freshness, event definitions, history, scope, source traceability and use. Report the status as **verified present**, **verified absent** or **not established**; do not infer absence from inaccessible systems.

If outcome measurements are genuinely unavailable, give a **prominent, normally high-priority recommendation** to establish a small, low-overhead, trustworthy dashboard or recurring report, with primary measures for **end-to-end demand-to-user lead time, real deployments, user-facing unavailability and actual recovery** (when incidents exist). Include relevant **DORA-oriented** views where events permit: **change lead time**, deployment frequency, change failure rate and recovery from failed deployments. Keep technical commit-to-production lead time **distinct from end-to-end lead time**. Use CI/CD, issue/work tracking, OpenShift releases, SLO/incident and customer evidence with clear definitions, source links, baselines and trends. Do not revive retired metrics as mandatory or invent missing rates.

An **existing usable dashboard** must be recognized; a dashboard's mere presence is **not itself an outcome**. If its existence cannot be verified, first recommend locating and validating the measures rather than claiming the team has none. For AI-driven work, insufficient measured results strongly constrains the assessment even when agent workflows look excellent.

A recommendation is part of the **initial** report, but actually constructing the dashboard or generating implementation/agent skills remains separately authorized, optional later work.

## Consequences

The assessment no longer overlooks missing measurement capability. Improvement is grounded in real outcomes, while avoiding metric theater, assumptions about tool availability or automatic reinstatement of the retired D05 deployment-rework metric.
