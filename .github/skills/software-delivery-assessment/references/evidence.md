# Evidence collection

Read only approved sources. Record exact file/revision, CI run, issue, deployment, incident or report reference, time window and limitations. Distinguish **observed** evidence from interview claims.

- **Requests and deliveries:** Locate genuine demand-arrival events and user-available delivery events; avoid treating first commit as end-to-end lead-time start. Validate production deployment counts and recovery/unavailability records.
- **Conditional diagnostics:** D03 requires identifiable changed deployments and linked failures. D09 requires a naturally maintained requirement-to-test relationship. If either is missing, ask one focused question; never fabricate a rate.
- **Code and tests:** Independently judge production code and tests. Inspect assertions and representative high-risk behavior, not merely file counts, coverage, mutation rate, TDD chronology or BDD scenario totals. Do not run tests without approval.
- **CI/CD and operations:** Inspect historical runs, promotion evidence, incidents and actual recovery—not only YAML configuration or written policy. Check consequential safeguards using recent examples.
- **Reports:** SonarQube, BonCode and similar external reports are supplemental. Record tool, version, revision, scope and exclusions. Verify representative findings. Do not equate vendor ratings or assume a scanner's presence means a release gate worked.
- **Interviews:** Ask only when a consequential unknown or contradiction remains. Separate statements from inspected evidence. Do not score missing access as poor performance.

Do not retrieve secrets, personal data or production payloads, run untrusted scripts, or modify products.
