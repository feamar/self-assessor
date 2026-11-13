# ADR-0034: End every perspective report with an explicit qualitative overall verdict

**Status:** Accepted — active  
**Extends:** [ADR-0030](0030-substantive-initial-expert-reports.md).

## Context

The first expert report test lacked a clear concluding judgment. An opening summary is insufficient when a detailed 5–10-page analysis has many caveats and findings; leadership needs a **final synthesized conclusion**.

## Decision

**End each perspective report with a prominent section titled "Final verdict"**. It must plainly say whether delivery is good enough for the selected perspective, identify the decisive supporting strengths and weaknesses, and end with an **explicit qualitative Overall score**. Example format:

> **Final verdict:** Delivery is progressing, but important improvements are still needed in measurement and release reliability. **Overall score: Satisfactory.**

This example is *illustrative*, not a default grade. Approved descriptors: **Excellent**, **Good**, **Satisfactory**, **Needs improvement**, **Unsatisfactory**, **Not demonstrated (insufficient evidence)**. Use natural professional language around the verdict. **Not demonstrated** represents inadequate evidence, not established poor delivery. Explain *why* the chosen descriptor is justified and how the result would change with better evidence or outcomes.

This is a **qualitative, evidence-grounded score**, not a return to weighted averages, numeric calculations or arbitrary thresholds. Continue to apply existing internal 0–10 evidence ceilings as non-formulaic guardrails; show a number only if explicitly requested. The final verdict is mandatory even when a report also starts with an executive judgment.

## Consequences

Every report has a clear conclusion that can be read by a lead developer or CTO without inference. Ratings remain candid and comparable in wording without false numerical precision.
