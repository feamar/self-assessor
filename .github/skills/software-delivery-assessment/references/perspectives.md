# Perspectives and score policy

The **same observed facts** apply to all perspectives. No backward-compatible legacy score is required.

## Delivery quality Q

Use applicable observed **D01–D24 and D26–D30** (29 common dimensions). D25 is AI-specific and excluded from Q.

`Q = 25 × sum(common scores) / count(scored applicable common dimensions)` (0–100). Report **coverage = scored / applicable** and whether the calculation is verified or provisional. Unknown dimensions do not count as zeros. Do not present a partial average as complete maturity.

A full headline requires at least **80% coverage** of applicable common dimensions **and inspected evidence for all applicable critical dimensions**. Otherwise label the value **partial / insufficient evidence**.

## AI-assisted A (six checks)

| ID | Capability to verify |
|---|---|
| A01 | Approved AI tools, data boundaries and permissions |
| A02 | Approved architecture/security standards guide generated changes |
| A03 | AI-assisted specification, TDD/BDD and independent test oracles |
| A04 | Human steering, accountable review and enforced approvals |
| A05 | Independent CI/test/security feedback on AI-authored changes |
| A06 | Measured impact, provenance and adverse-trend transparency |

## AI-driven R (seven checks)

| ID | Capability to verify |
|---|---|
| R01 | Bounded multi-step agency with observed task outcomes |
| R02 | Versioned approved policy and context grounding |
| R03 | Independent specifications/tests detect generated faults |
| R04 | Sandboxes, least privilege and prompt-injection protections |
| R05 | Independent build/test/security gates; no self-approval |
| R06 | Traceable changes, accountable promotion and rollback |
| R07 | Production results, incidents and continuous validation |

Rate readiness checks 0–4 with the same evidence anchors as dimensions. **Confirmed absence of AI integration** means readiness 0, not lower Q. **Unknown AI use** means unknown readiness, not 0. Readiness averages: `A = 25 × mean(scored A checks)`; `R = 25 × mean(scored R checks)`. State coverage. D25 must be evidenced for a full AI headline.

## Perspective scores

- **Conventional:** `Q`
- **AI-assisted:** `0.60 × Q + 0.40 × A`
- **AI-driven:** `0.50 × Q + 0.50 × R`

Weights are **assessor policy**, not empirically validated benchmarks. Report selected perspective first and the other computable perspectives for context. For an AI headline require full common-dimension coverage threshold, all applicable readiness checks assessed, and D25 evidenced; otherwise label it partial. Never claim a verified score from interview-only evidence. Show critical findings separately regardless of arithmetic.
