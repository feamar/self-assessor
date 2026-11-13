# Report format

**Default: short and decision-ready.** Provide a detailed ledger or JSON only if requested or necessary to make a disputed score auditable.

## Summary

- **Scope:** service, repository/commit, assessment dates, sources available/missing.
- **Selected perspective:** score /100 or **partial / insufficient evidence**, verified/provisional, and coverage. Show other computable perspectives in one line.
- **Verdict:** 2–4 sentences on delivery quality and uncertainty.
- **Critical risks:** blocking findings with evidence IDs; never hide behind averages.
- **Code quality:** separate, evidence-backed judgment with sampled examples.
- **Test quality:** separate, evidence-backed judgment with sampled examples.
- **Next actions:** 3–5 prioritized, specific verification or improvement steps, with expected benefit.

## Scorecard

For **all 30 dimensions**, record `ID | 0–4 / unknown / N/A | verified / provisional | evidence IDs | concise rationale`. Include readiness A01–A06 and R01–R07 when relevant. Group rows by delivery, testing, architecture/security, reliability and AI. Show coverage and score calculations, with actual denominators.

## Evidence ledger (on request)

For each finding: evidence ID, type (O/X/P/E/I/C), exact source (path and lines, URL/run ID or report page), revision/date range, what it demonstrates, limitations, contradictions and confidence. Include executed commands only when authorized and actual results, not invented outputs. For imported reports, show disagreements and scan-scope mismatches. Preserve uncertainty and distinguish claims from direct observation.

## Decision rule

A partial numeric value is an **observed-only illustration**, never a full verified maturity score. Critical failures are reported regardless of average. Do not call the output an independent certification, compliance determination or penetration test.
