# ADR-0025: Consolidate the currently active judgment and report policy

**Status:** Accepted — active  
**Supersedes:** [ADR-0020](0020-calibrated-qualitative-perspectives.md) and [ADR-0021](0021-three-paragraph-report.md) as complete documents. Their substantive calibration and brevity rules remain here; their older one-perspective wording is obsolete.  
**Consistent with:** [ADR-0023](0023-candid-evidence-specific-feedback.md) and [ADR-0024](0024-all-perspectives-separate-outcomes.md).

## Context

ADR-0024 superseded only part of ADR-0020's original one-perspective execution decision and clarified ADR-0021's reporting scope. Keeping partially active documents obscured what was authoritative. We want **active and inactive decisions to be unambiguous** while retaining historical rationale.

## Decision

**Always assess all three perspectives** from the same evidence: conventional, AI-assisted and AI-driven. Produce **three independent Markdown outcome files**, each **no more than three concise paragraphs or one page** and suitable for both lead developers and CTOs. The user selects which completed judgment is displayed; default to conventional. Preserve all three, and do not overwrite historic assessments silently.

Offer a clear **qualitative, evidence-grounded judgment with candid reasons**, not a printed numeric rating or weighted composite by default. A requested numeric rating uses professional calibration, not an average:

- **No credible outcome-oriented evidence:** maximum indicative **4/10**.
- **Current objective outcomes but no sustained documented success:** maximum indicative **8/10**.
- **Strong and independently checkable history of repeatable success:** **9/10** may be deserved.
- **Exceptional sustained evidence of engineering/reliability comparable in substance to strong Google engineering circa the mid-2010s and mature SRE:** **10/10** may be deserved.

These are **ceilings, not a scoring algorithm**. The report explains (1) verdict and observed outcomes, (2) evidence, risks and confidence, (3) practical next steps or—if genuinely excellent—why the system should **keep doing what works**. Critical security, privacy and release risks remain visible regardless of performance.

Outcome documents or agent skills are **drafted as separate artifacts** if target repository writes are not authorized. Saving them into that repository or executing work requires explicit permission.

## Consequences

ADR-0020 and ADR-0021 become **inactive/superseded** without losing their historical record. This ADR is the active source for their surviving calibration and reporting constraints. ADR-0023 continues to govern candid feedback and ADR-0024 the all-perspective output workflow.
