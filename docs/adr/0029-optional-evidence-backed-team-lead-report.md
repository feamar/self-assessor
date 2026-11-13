# ADR-0029: Optional evidence-backed detailed report for team leads

**Status:** Accepted — active  
**Extends:** [ADR-0025](0025-consolidated-judgment-and-report-policy.md), [ADR-0028](0028-evidence-first-report-before-optional-agent-skills.md)

## Context

The required three-paragraph perspective judgments are suitable for lead developers and CTOs, but a team lead may need **more actionable detail**: exactly which concerns the evidence reveals, why those findings are consequential, and how to resolve or verify them. Automatically including this material would undermine the concise default report. Tying it to agent-skill generation would misprioritize remediation over evidence and reporting.

## Decision

After the assessor has **gathered evidence and completed all three perspective-specific Markdown judgments**, it should **offer, but not automatically generate**, an optional **detailed team-lead findings report**. Produce it only on explicit request, as a **separate Markdown artifact**, not an expansion of the executive judgment. The three-paragraph/one-page ceiling remains in force **only for the original perspective judgments**.

The detailed report should use the already collected evidence and, for each material concern, specify **(1) the concern, (2) the exact evidence and confidence, (3) why it creates delivery, customer, quality or risk consequences, (4) specific prioritized improvements and (5) how to verify improvement**. Include scope, sources, limitations and material strengths as appropriate. Clearly distinguish observed defects, credible risks, and missing evidence; do not invent findings, use arbitrary numerical severity, or blame individuals. Organize by significance and avoid reproducing all 18 dimensions mechanically.

When additional evidence would materially affect a concern, ask a targeted follow-up or mark it unknown. Do **not** rerun the assessment, request unrelated data, or treat missing SonarQube/pipeline history as proof of poor performance.

This **optional detailed report is independent of optional agent instructions**: it neither creates SKILL.md files nor requires that feature. Writing the detailed report to the assessed repository or executing recommendations requires separate authorization.

## Consequences

The default user experience remains **three concise, candid reports**, showing the selected one. A team lead can later obtain an evidence-traceable, actionable explanation without repeating collection or sacrificing brevity. Agent instructions remain an additional, separately requested follow-up. The reference [team-lead-report.md](../../.github/skills/software-delivery-assessment/references/team-lead-report.md) defines the report's content.
