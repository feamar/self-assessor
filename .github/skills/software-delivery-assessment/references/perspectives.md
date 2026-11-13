# Calibrated perspective-specific judgments

Choose **one perspective** (conventional by default). Issue a **qualitative judgment with rationale**, not an arbitrary arithmetic score, weighted perspective average or dimension roll-up. Only state a numeric grade when explicitly asked.

## Internal 0–10 calibration (never a formula)

| Evidence situation | Highest defensible indicative grade |
|---|---|
| No credible **outcome-oriented evidence**, even with impressive practices or interviews | **4/10**: actual delivery effectiveness is not demonstrated |
| Credible **current objective outcomes**, but no documented sustained track record of success | **8/10**: judge code, tests, practices, security and operational capability pragmatically |
| Strong, independently checkable **history of repeated success** in production and user outcomes | **9/10** is possible, not automatic |
| Exceptional, sustained results comparable in substance to strong **Google engineering circa the mid-2010s and mature Google SRE** | **10/10**, exceptionally |

Ceilings are guardrails, not targets. *Without evidence* in the 8 ceiling means **without a long-term documented trail**, **not without outcome evidence** (which caps the grade at 4). The exact grade between 4 and 8 is less important than describing successful outcomes, process reliability and limitations. A functioning product, apparently low cost, fast releases or known happy customer matters when credible, but does not alone establish repeatability and improvement. A critical unmitigated risk can warrant a much weaker verdict than the ceiling.

## Conventional — demanding human-led engineering

Benchmark strong Google-style engineering practices from roughly ten years ago and mature SRE: maintainable code, effective testing and review, reproducible builds/releases, security, monitoring, clear user-facing SLOs, operational response, rollback, incident learning and verified outcomes. Human developers have no agent leverage but may understand the whole codebase more deeply. Acknowledge workload; **do not lower reliability or security expectations**.

## AI-assisted — demand more from agent leverage

Developers can delegate research, implementation, testing and repetitive tasks. Expect greater delivery capability and stronger verification than for purely human-led development, **not AI adoption for its own sake**. Require demonstrated impact on quality, speed/cost or reliability plus approved context, human accountability, effective independent test oracles and enforced security/release gates. Recommend task-specific skills agents can execute.

## AI-driven — highest standard of results and independent controls

Agents do most work: demand **strongest measurable results and sustained trends**, along with scoped permissions, sandboxes, independent quality gates/oracles, provenance, change authorization, recovery and telemetry. Process activity is not proof of delivered value. **Without measured outcomes**, issue a sharply limited judgment (4 ceiling) and propose a rigorous **instrumentation skill** defining and measuring request-to-user lead time, genuine deployments, user-facing failure/recovery and availability, quality and relevant cost, with provenance, baselines and a review cadence.

All perspectives see the same observations; the required standard rises with automation. Do not project hypothetical improvements as measured facts.
