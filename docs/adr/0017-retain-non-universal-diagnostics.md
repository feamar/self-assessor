# ADR-0017: Retain non-universal diagnostics D09 and D14

**Status:** Accepted  
**Decision:** Retain D09 and D14 as optional diagnostics, despite not meeting the universal metric-strength criterion.

## Context

The assessment prioritizes simple, hard-to-game, outcome-oriented, universal and transparent metrics. **Universal** means that the underlying measurement principle transfers across different fields (with different terminology where necessary). Universality is a strength, but a specialist diagnostic can still help explain delivery performance or reveal a consequential verification risk.

- **D09 — Requirement-to-test linkage:** Depends on identifiable requirements, executable tests and meaningful links. Such artifacts are not inherent to every kind of work. When those links are naturally maintained, the ratio is straightforward to obtain. It is a *process proxy*, not a delivery outcome.
- **D14 — Test flakiness:** Requires repeatable test executions whose results can vary independently of relevant changes. This is especially useful for automated software verification, but the measurement is not transferable to every domain.

## Decision

Retain both metrics as **non-universal, optional diagnostics**. Do not remove them solely for limited universality. Use D09 only when meaningful requirement/test links already exist; otherwise ask how an important requirement is verified. Use D14 when rerun/failure evidence makes unstable feedback observable; otherwise inspect or ask about material verification reliability.

Neither metric is part of the universal **primary outcome** set. Neither is a mandatory questionnaire item, an individual maturity score, or a required process target.

## Consequences

The assessment remains concise and outcome-first while preserving valuable specialist evidence. The report labels D09 and D14 as diagnostic and specifies their scope and source. Absence of an applicable process or usable evidence is **N/A or unknown**, not a poor result. Do not encourage superficial trace links or unnecessary reruns to inflate a metric. Reconsider the exception only if these diagnostics prove unhelpful in actual assessments.
