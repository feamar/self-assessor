# ADR-0030: Substantive initial expert reports with complete rationale

**Status:** Accepted — active  
**Supersedes:** [ADR-0024](0024-all-perspectives-separate-outcomes.md), [ADR-0025](0025-consolidated-judgment-and-report-policy.md), [ADR-0029](0029-optional-evidence-backed-team-lead-report.md).  
**Preserves:** Separate conventional, AI-assisted and AI-driven judgments; common evidence base; user-selected display; qualitative evidence calibration and optional later agent instructions.

## Context

The first assessment test showed that **three-paragraph executive outputs were insufficient**. The reasoning, technical interpretation, evidence, weaknesses and opportunities needed to be present in the **initial report**, rather than accessible only through an optional team-lead follow-up.

## Decision

Every run must generate **three independent, well-formatted Markdown expert reports**, one per perspective, each targeting **5–10 printed pages** where evidence is sufficient. The developer selects which report to see (default conventional); the other two remain available without reassessing. The target is substantive depth, not padding: with insufficient evidence, use fewer pages and explicitly explain uncertainty.

Each initial report includes an executive verdict, scope and sources, actual production and delivery outcomes, code/test/CI/CD/operational evidence, relevant OpenShift/GitOps traces, explicit material findings and strengths, **a full expert explanation of why the verdict is deserved**, a distinction between confirmed impact and hypothesized risks, and **specific prioritized improvements with evidence-based verification**. Use readable headings, selective tables, dated references and clear confidence statements. An excellent system receives exact recognition and encouragement to keep it up; underperforming delivery receives candid practical feedback. Do not reduce all 18 dimensions to arithmetic scores.

Keep **qualitative grading**; print numbers only on request. The internal evidence ceilings remain: **no outcome evidence ≤4/10**, current outcomes without a sustained documented record **≤8/10**, **9/10** only for strong repeated documented success and **10/10** only for exceptional sustained results comparable to strong mid-2010s Google engineering and mature SRE. These are calibration guardrails, never weighted computations.

The optional team-lead output, if requested after reporting, now adds **deeper technical implementation detail**, not the expert reasons missing from the initial report. Optional agent skills remain a separate post-report choice. Product access is read-only by default, with explicit permission required for writing or execution.

## Consequences

Initial output is longer, better structured and more explanatory. It remains evidence-first and perspective-specific, with no fabricated metrics or mandatory filler. ADRs 0024, 0025 and 0029 become inactive so the ADR index has one clear current reporting contract.
