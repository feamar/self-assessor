# Evidence collection

**Evidence is the assessment's first priority.** Read only approved sources. Record exact file/revision, CI run, issue, deployment, incident or report reference, time window and limitations. Distinguish **observed** evidence from interview claims.

## Early evidence-source conversation

After inspecting the accessible workspace, **proactively ask once** if the developer can point you to the most valuable missing sources. Keep it short and conversational, not a mandatory form:

> Can you point me to CI/CD and deployment history, **any delivery/DORA metrics dashboard or recurring report**, SonarQube or other quality reporting, test and monitoring/incident results, and **OpenShift synchronization/rollout logs if used**? **Is there other evidence we should examine**—customer feedback, change requests, support data or costs? Approved links or redacted exports are fine.

Use what is already available instead of making the developer repeat it. Follow up only for evidence that would materially change a judgment. If sources are unavailable, finish the assessment with **explicit evidence limitations**; do not assume either good or bad performance.

## Evidence priorities

1. **Delivered results and measurement visibility:** Request/demand and user-available delivery records, genuine production deployment events, reliability/SLO dashboards, incidents/recovery, service costs and customer outcomes. **Explicitly locate or ask about a DORA/delivery performance dashboard**, report or recurring extract, and validate freshness, event definitions, time windows, source provenance and actual use. Classify **present / absent / unknown** rather than assuming a missing link means no dashboard. Seek trends, not anecdotes.
2. **CI/CD history:** Build/test pipeline **runs**, actual checks and failures, gate decisions, promotions/deployments and release traceability. A pipeline configuration does **not** demonstrate historical execution or effectiveness.
3. **Quality and tests:** SonarQube or equivalent code-quality and security results, BonCode/other reports if provided, test runs, defect trends and representative code/test inspection. Corroborate findings with the assessed revision and actual release gating; don't blindly trust vendor scores.
4. **OpenShift/GitOps synchronization and release events where applicable:** Inspect approved read-only OpenShift GitOps/Argo CD sync and controller history, Flux reconciliations or equivalent deployment events, retries/errors/drift and rollout/health records. Map time, app/namespace/environment, source/manifest revision and sync/rollout result to CI promotion and actual production availability. **Synchronization is not deployment, successful release or user outcome**. Beware clock skew, incomplete log retention and manual overrides.
5. **Other evidence:** Issue tracking, support tickets, user feedback, incident reviews, financial/effort evidence and relevant architecture/security rules. Treat interviews as provisional unless corroborated. **Ask whether any other meaningful source exists** before finalizing, then finish with explicit limitations if unavailable.

Retain a traceable **evidence ledger** of source references, revision/date, periods, observations, confidence and disagreement. Include whether the DORA/delivery dashboard and core outcome measurements were **verified, unavailable or not established**, and the evidence behind that status. Feed it directly into the **initial expert reports**, not just an optional appendix. Distinguish demonstrated concerns from unverified risks or unknowns; do not publish private data in the report.

Request permission before accessing external/cluster systems or running CLI commands. OpenShift and GitOps logs may contain tokens, internal URLs, environment variables or protected information; prefer approved read-only views or sanitized exports. **Never request credentials, secrets or raw confidential payloads**. Missing OpenShift access is an evidence gap, not proof of a failed synchronization.

- **Requests and deliveries:** Locate genuine demand-arrival events and user-available delivery events; avoid treating first commit as end-to-end lead-time start. Validate production deployment counts and recovery/unavailability records.
- **Conditional diagnostics:** D03 requires identifiable changed deployments and linked failures. D09 requires a naturally maintained requirement-to-test relationship. If either is missing, ask one focused question; never fabricate a rate.
- **Code and tests:** Independently judge production code and tests. Inspect assertions and representative high-risk behavior, not merely file counts, coverage, mutation rate, TDD chronology or BDD scenario totals. Do not run tests without approval.
- **CI/CD and operations:** Inspect historical runs, promotion evidence, incidents and actual recovery—not only YAML configuration or written policy. Check consequential safeguards using recent examples.
- **Reports:** SonarQube, BonCode and similar external reports are supplemental. Record tool, version, revision, scope and exclusions. Verify representative findings. Do not equate vendor ratings or assume a scanner's presence means a release gate worked.
- **Interviews:** Ask only when a consequential unknown or contradiction remains. Separate statements from inspected evidence. Do not score missing access as poor performance.

Do not retrieve secrets, personal data or production payloads, run untrusted scripts, or modify products.
