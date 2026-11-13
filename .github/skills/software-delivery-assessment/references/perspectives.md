# Three perspectives

All three perspectives share the **same observed delivery outcomes** from [metrics](metrics.md). Do not compute arbitrarily weighted composite scores.

| Perspective | Question to answer | Additional assurance |
|---|---|---|
| **Conventional** | How quickly, correctly and reliably can this system deliver change? | Code/test effectiveness, security, architecture, release and operational controls |
| **AI-assisted** | Can people use AI while retaining the same outcomes and independent quality/security guarantees? | Approved tools/data, architecture grounding, human accountability, independent tests and CI gates, provenance and measured impact |
| **AI-driven** | Can bounded agents deliver changes under independent verifiable controls? | Scoped context, sandboxing, least privilege, prompt-injection defenses, independent specifications/tests, no self-approval, accountable promotion, rollback and telemetry |

## Evidence expectations

- Report actual outcome measures once, then **perspective-specific capabilities, gaps and risks**. Do not present hypothetical AI improvements as measured results.
- AI-assisted checks: approved tools/permissions; approved engineering rules; independent tests/oracles; human approval where required; CI/security gates; provenance and impact.
- AI-driven checks: proven bounded autonomy; approved policy/context; independent verification; sandbox/permissions; non-bypassable gates; accountable release/rollback; production feedback.
- Distinguish **verified**, **provisional**, **unknown** and **N/A** judgments. No AI use does not reduce conventional delivery quality; AI readiness may still be absent or unassessed.
