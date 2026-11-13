# ADR-0020: Qualitative perspective judgments with evidence ceilings

**Status:** Superseded / inactive — see [ADR-0025](0025-consolidated-judgment-and-report-policy.md)

## Context

Weighted combinations of dimensions obscure actual delivery capability. Conventional human-led, AI-assisted and AI-driven delivery have different expectations.

## Decision

Use a **qualitative, reasoned judgment** from one selected perspective; no weighted averages or automatic printed number. If a number is explicitly requested, use a *non-formulaic* 0–10 calibration: **no outcome evidence caps grade at 4**; **credible current results but no sustained documented history cap it at 8**; **9 requires documented repeated success**; **10 is reserved for exceptional sustained Google engineering/SRE-level performance**. Mid-range distinctions are secondary to a convincing rationale.

Conventional expects strong engineering and SRE with human effort and whole-codebase knowledge. AI-assisted must deliver more with agent leverage and independent quality safeguards. AI-driven demands the highest measured outcomes and independent agent governance; without outcome evidence require a rigorous measurement proposal.

## Consequences

No composite score, formula, AI adoption bonus or invented metrics. Evidence, customer results, cost, code/test quality and critical risks determine the explanation. Numerical calibration remains an internal guardrail unless requested.

**Updated by [ADR-0024](0024-all-perspectives-separate-outcomes.md):** the one-selected-perspective execution rule is superseded. All three perspectives now run; the evidence calibration remains valid.

**Historical note:** ADR-0025 is now the authoritative home of the surviving evidence-calibration rules and the three-perspective workflow. This file is retained for the audit trail, not as current instructions.
