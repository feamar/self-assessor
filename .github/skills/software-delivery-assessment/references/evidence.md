# Evidence collection

**Evidence is the assessment's first priority.** Read only approved sources. Record exact file/revision, CI run, issue, deployment, incident or report reference, time window and limitations. Distinguish **observed** evidence from interview claims.

## Early evidence-source conversation

After inspecting the accessible workspace, **proactively ask once** if the developer can point you to the most valuable missing sources. Keep it short and conversational, not a mandatory form:

> Can you point me to the CI/CD pipeline and deployment history, SonarQube or other code-quality reporting, and any test, monitoring or incident results? URLs, report exports or an approved read-only way to access them are fine.

Use what is already available instead of making the developer repeat it. Follow up only for evidence that would materially change a judgment. If sources are unavailable, finish the assessment with **explicit evidence limitations**; do not assume either good or bad performance.

## Evidence priorities

1. **Delivered results:** Request/demand and user-available delivery records, genuine production deployment events, reliability/SLO dashboards, production incidents and recovery, service costs and customer outcomes where available. Look for multi-period trends, not anecdotes.
2. **CI/CD history:** Build/test pipeline **runs**, actual checks and failures, gate decisions, promotions/deployments and release traceability. A pipeline configuration does **not** demonstrate historical execution or effectiveness.
3. **Quality and tests:** SonarQube or equivalent code-quality and security results, BonCode/other reports if provided, test runs, defect trends and representative code/test inspection. Corroborate findings with the assessed revision and actual release gating; don't blindly trust vendor scores.
4. **Supporting records:** Issue/requirement tracking, incident reviews, operational logs and relevant architecture/security rules or exceptions. Treat interviews as provisional unless corroborated.

Retain a concise **evidence ledger** of references, source revision/date, period, finding and confidence where possible, so a later requested detailed team-lead report can be prepared **without repeating the assessment or inventing evidence**. Distinguish demonstrated concerns from unverified risks or unknowns; do not publish private data in the report.

Request necessary approval before opening external systems. Accept read-only URLs or sanitized report exports; **never request credentials or confidential payloads**.

- **Requests and deliveries:** Locate genuine demand-arrival events and user-available delivery events; avoid treating first commit as end-to-end lead-time start. Validate production deployment counts and recovery/unavailability records.
- **Conditional diagnostics:** D03 requires identifiable changed deployments and linked failures. D09 requires a naturally maintained requirement-to-test relationship. If either is missing, ask one focused question; never fabricate a rate.
- **Code and tests:** Independently judge production code and tests. Inspect assertions and representative high-risk behavior, not merely file counts, coverage, mutation rate, TDD chronology or BDD scenario totals. Do not run tests without approval.
- **CI/CD and operations:** Inspect historical runs, promotion evidence, incidents and actual recovery—not only YAML configuration or written policy. Check consequential safeguards using recent examples.
- **Reports:** SonarQube, BonCode and similar external reports are supplemental. Record tool, version, revision, scope and exclusions. Verify representative findings. Do not equate vendor ratings or assume a scanner's presence means a release gate worked.
- **Interviews:** Ask only when a consequential unknown or contradiction remains. Separate statements from inspected evidence. Do not score missing access as poor performance.

Do not retrieve secrets, personal data or production payloads, run untrusted scripts, or modify products.
