# Calibrated perspective-specific judgments

**Always evaluate all three perspectives in each run.** Share the evidence collection, but reason separately for conventional, AI-assisted and AI-driven delivery. Each perspective produces its own qualitative judgment. The user's choice determines which judgment is **displayed**, not which are evaluated. Default display: conventional. No weighted formulas, maturity averages or numeric grades unless expressly requested.

## Internal 0–10 calibration (not default output)

| Evidence | Maximum indicative grade |
|---|---|
| No credible outcome-oriented evidence | **4/10**, even with plausible practices or interviews |
| Credible current outcomes but no documented sustained success | **8/10** |
| Strong, independently checkable history of repeated success | **9/10** possible, not automatic |
| Exceptional sustained results comparable in substance to strong Google engineering circa the mid-2010s and mature Google SRE | **10/10**, exceptionally |

These are ceilings, not a calculation. The 8 ceiling **requires some objective outcome evidence**; absent that, the 4 ceiling applies. Critical risks can justify weaker judgments.

## Conventional: demanding human-led delivery

Judge against strong Google-style engineering of roughly ten years ago and mature SRE: reliable, maintainable code, meaningful tests and review, reproducible releases, security, operational observability, user-facing service levels, recovery, learning and demonstrated outcomes. Developers do more themselves without agents but may know the whole codebase better. Recognize that work while maintaining demanding quality and reliability expectations.

## AI-assisted: higher expectations through delegation

Developers can delegate investigation, implementation, testing and routine work. Demand stronger delivery capability and independent verification than for conventional teams—not AI adoption as a goal. Verify real impact on speed, cost, reliability and test/security outcomes; appropriate permissions, human accountability and independent gates are essential.

## AI-driven: highest bar and measurable results

Agents perform most work. Demand the strongest demonstrated outcomes and trends, independent test oracles, bounded privileges, provenance, non-bypassable release controls, recovery and telemetry. Without measured output, give a sharply limited verdict (internal ceiling 4) and **explain the need for rigorous measurement/instrumentation** with event definitions, data provenance, baselines and ongoing review. **Do not draft an agent skill before reporting; offer that as an optional subsequent step.**

## Be candid, proportionate and useful

- **Weak:** Say plainly that delivery is below the expected standard; identify observed failures or evidence gaps, consequences and the few changes that matter most. Avoid euphemisms. Judge delivery systems, not individuals.
- **Good:** Give **earned praise** tied to specific observed results or practices, while pointing to credible further gains and how to achieve them.
- **Excellent:** Identify precisely which **sustained, independently substantiated results** meet the gold standard, and tell the team to **keep it up**. Do not invent weaknesses or compulsory improvement tasks.
- **Unproven:** If evidence is insufficient, say that success cannot be established—not that the team is poor or excellent.

Do not copy the same judgment three times with different labels: differences in required capability and assurance should materially affect each perspective. Never invent measurements or claim hypothetical gains as actual results.
