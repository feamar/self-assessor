# ADR-0031: Inspect OpenShift synchronization and ask for additional evidence

**Status:** Accepted — active  
**Extends:** [ADR-0028](0028-evidence-first-report-before-optional-agent-skills.md), [ADR-0030](0030-substantive-initial-expert-reports.md).

## Context

Repository inspection, pipeline configuration and static code-quality reports cannot by themselves establish what reached production. OpenShift/GitOps reconciliation and synchronization records provide additional evidence of release flow, drift and failure. The lead developer may also know other important evidence sources that a fixed checklist misses.

## Decision

Where applicable, **ask to inspect OpenShift synchronization/reconciliation history and related rollout evidence**: OpenShift GitOps/Argo CD application synchronization status and history, controller/events or redacted logs, Flux reconciliations, OpenShift rollout/deployment history, errors/retries/drift and runtime health. Record actual timestamp, relevant app/environment/namespace, manifest/Git revision and status. **Correlate synchronization with CI/CD promotion, actual deployment, service readiness and user impact**; do not equate a green synchronization with an effective release or delivered user value.

When seeking CI/CD, SonarQube, test, operational and user evidence, explicitly ask **"Is there any other relevant evidence we should examine?"** Examples include support tickets, costs, incident reviews and customer outcomes. Avoid repetitive mandatory questionnaires or irrelevant sources. Require authorization for external/cluster access; do not ask for credentials, secrets or unredacted sensitive logs. If unavailable, report evidence gaps and uncertainty rather than assuming failure.

## Consequences

The assessment can detect sync/rollout problems that were invisible to code-only reviews and can use unanticipated project-specific evidence. More evidence does not change the core requirement to judge **outcomes**, not mere process events.
