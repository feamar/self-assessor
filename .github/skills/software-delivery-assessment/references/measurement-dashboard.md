# Delivery outcomes and DORA-oriented measurement dashboard

**Required investigation and report topic.** A strong delivery assessment should ask where the delivery metrics actually live and how the team learns whether changes help. **A dashboard is an enabling feedback mechanism, not an outcome metric, compulsory technology or proof of effectiveness.**

## Investigate an existing dashboard before recommending a new one

Look for dashboards, SRE service reports, DORA views, historical exports or other recurring evidence. Ask the developer for links or approved read-only access if the available project history does not reveal them. Distinguish:
- **Verified present:** You inspected a dated, traceable, sufficiently current dashboard/report and its supporting sources.
- **Verified absent:** An accountable source confirms the team has no usable recurring measurements or relevant records; cite this evidence.
- **Not established:** No dashboard or metrics were accessible/confirmed. Do **not** assert that the team has none.

Examine event definitions, source system, environment and service scope, history/retention, timestamps, units, sampling, denominator, data quality and freshness. Check whether the dashboard influences delivery decisions and whether leading candidates are simple, transparent and hard to game. A beautiful dashboard with incorrect or unused numbers is not a high-performing system.

## Minimal useful measures

Start small with naturally occurring, trustworthy events—not an 18-metric collection project:

| Concern | Minimum practical measure and evidence |
|---|---|
| **End-to-end delivery speed (our primary D01)** | Real request accepted/intake timestamp → requested capability actually available to users; median and spread where sample supports it |
| **Deployment frequency (D02)** | Actual successful production releases per service and period, backed by deployment/rollout/release evidence |
| **User-facing reliability (D22)** | Actual core-service unavailability and meaningful SLO/user-impact records |
| **Recovery time (D04)** | User-impacting failure → restored useful service for real incidents only; if none observed, label **not observed**, not zero |
| **Change failure rate (D03 diagnostic)** | Production change → attributable incident, rollback or urgent remediation, only if linked events can be verified |
| **Detection time (D23 diagnostic)** | User impact → operational detection for actual incidents, if timestamps are trustworthy |

Where useful also display the familiar **DORA-oriented view** with **change lead time** (commit/change-to-production, clearly distinguished from our **end-to-end request-to-user lead time**), deployment frequency, change failure rate and failed-deployment recovery. Map labels and event definitions explicitly; do **not** claim all DORA metrics are identical to the current four primary outcome measures. Do not restore retired metrics (e.g. deployment rework) as compulsory scores.

## Concrete recommendation if measurement is genuinely missing

Recommend a **small, low-overhead, regularly reviewed dashboard or equivalent report**, using existing **issue tracker/demand records, Git and CI/CD runs, OpenShift/GitOps history, production release events, incidents, monitoring/SLOs and user acceptance records**. First verify source timestamps and correlation; a green GitOps sync does **not** equal a production delivery or healthy user service. Show trends over real periods with drill-down to source IDs, representative outliers and explicit **unknown** values. Prefer a trustworthy manually assembled baseline over an automated but misleading scorecard. Record a baseline and a simple review rhythm, then test whether subsequent interventions actually improved user outcomes, delivery speed, recovery or quality.

If these results cannot be measured, **raise the improvement prominently**—often near the top of the ranked ten, especially for AI-driven delivery where observed outcomes are central. If dashboard status is merely unverified, rank **find and validate the existing measurements** first rather than asserting an absent dashboard.

The agent may **recommend** the measurement work within the initial report but must **not build a dashboard, deploy instrumentation or create an agent skill by default**. Such execution requires a later explicit request and authorization.
