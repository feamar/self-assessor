# Optional detailed team-lead findings report

**Use only on demand, after the three perspective judgments have been generated.** This document is a **separate Markdown report** for the team lead, based on the same inspected evidence; it must not replace or lengthen the three short executive judgments. It is **not an instruction to generate remediation agent skills**.

## Purpose and audience

Explain clearly **what is concerning, why it matters and how to improve it** so a team lead can direct practical engineering work. Be candid about demonstrable shortcomings, proportionate about risk, and specific about what already works. No arbitrary weighted score, generic maturity rubric, mandatory checklist or fabricated findings. Choose an informative filename such as `assessment-team-lead-findings.md` (add date/service identifier if needed); don't silently overwrite previous results.

## Required content

Start with **scope and evidence basis**: service, revision, assessment period, sources consulted (e.g. CI/CD execution history, quality gates, SonarQube/code reports, tests, production metrics), inaccessible sources and material limitations. Note which perspective(s) the concerns affect.

For each **material concern** grounded in evidence, include:

1. **Concern and priority:** a short, concrete description and qualitative urgency, based on user/delivery/security impact and not an arbitrary numeric severity.
2. **What was observed:** precise source references such as pipeline/run IDs, report dates and findings, commit/file references, incident IDs, relevant events and time windows. State whether evidence is **verified, corroborated, provisional or unavailable**.
3. **Why it is concerning:** the causal connection to delivery speed, correctness, reliability, customer impact, security, maintainability or effectiveness of independent verification. Distinguish actual impact from plausible risks and avoid speculative causal claims.
4. **What to do:** a specific, proportionate action or investigation. Prefer remedies with a clear mechanism and minimal process overhead. Identify relevant dependencies and ownership *roles* where justified, not individuals to blame.
5. **How to know it improved:** observable verification, a meaningful outcome trend or a demonstrable risk-control test. State what additional access or facts would resolve important uncertainty.

Group related concerns, rank the few most consequential first, and avoid duplicate sections for the three perspectives where one issue affects all. **Differentiate code quality from test quality.** Important confirmed strengths can be summarized briefly to preserve context. When the evidence supports **no material concerns**, explicitly say so; don't create issues to fill a report.

## Evidence and scope boundaries

Use the evidence already gathered during the assessment. **Do not re-run the entire assessment** to create this report. Request an additional pipeline/report/incident source only if a consequential uncertainty needs resolution, and proceed with clearly identified unknowns if access is unavailable. A missing report or metric is an **evidence limitation**, not proof that the team's process is poor. Never promote vendor scores, pipeline configuration, policy documents or interview assertions into verified outcomes without corroboration.

This report may exceed one page: clarity and traceability matter more than an artificial word limit. It should remain focused on decisions a team lead can act on.

## Optionality and permissions

**Never draft this report by default.** Offer it after the original three judgments; create it only when the developer/team lead requests it. Deliver a standalone Markdown artifact or copy-ready text. Writing it into the assessed repository needs separate permission. **Do not also generate future agent SKILL.md files** unless that is separately requested. Any proposed remediation execution also requires authorization.
