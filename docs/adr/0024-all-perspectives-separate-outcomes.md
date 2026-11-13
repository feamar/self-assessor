# ADR-0024: Evaluate all three perspectives and preserve separate outcome documents

**Status:** Accepted

## Context

Evaluating only a selected perspective wastes shared evidence and makes comparison dependent on repeated assessments. The user wants all three expert judgments retained while displaying only the perspective they choose.

## Decision

Every run assesses **conventional, AI-assisted and AI-driven** delivery using the **same evidence collection** but each perspective's distinct expectations. Produce **three independent outcome files**, with **Markdown as the default format**; the assessor chooses suitable filenames and location for the assessed service. Each file records the perspective, service/revision, period, evidence anchors and a judgment of **no more than three paragraphs / one page**.

The user's choice controls **which outcome is shown**, not which is evaluated; display conventional by default when no preference is given. Identify the two other files and support selection later **without rerunning**. Do not silently overwrite previous assessments.

The assessed repository remains read-only unless writing is authorized. Without authorization, prepare **three separate copy-ready Markdown artifacts**, explicitly distinguishing these from committed files. Applying improvement skills or modifying product code requires separate permission.

## Consequences

The model does additional perspective reasoning once per assessment but preserves all findings for later comparison. This decision **supersedes only the earlier one-selected-perspective execution rule** in ADR-0020 and ADR-0021. Their evidence thresholds and three-paragraph limit remain in force.
