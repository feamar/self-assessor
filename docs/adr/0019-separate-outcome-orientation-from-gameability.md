# ADR-0019: Separate outcome orientation from gameability

**Status:** Accepted

## Context

The assessment retained 18 active dimensions, but only four are primary outcome metrics. Four are optional diagnostics or diagnostic questions; ten are assurance questions. Calling all 18 "metrics", or referring to only four without distinguishing the layers, obscures what is being assessed.

Two of the metric-strength criteria were also conflated. A metric can measure an outcome while still being gameable, or track a prescribed process that is not outcome-oriented.

## Decision

1. Always distinguish **18 active dimensions** from their contents: **4 primary outcome metrics, 4 optional diagnostics/diagnostic questions and 10 essential assurance questions**. Do not imply that all are numerical metrics.
2. Assess **outcome oriented** by asking: *Does the metric measure a result, rather than conformance with a prescribed process?*
3. Assess **hard to game** separately by asking: *Can optimizing the metric improve its numerical value without improving the intended result or capability?*
4. Do not use either criterion as a proxy for the other. Apply both to each candidate metric.

For example, D09 requirement-to-test linkage measures process traceability, so it is **not outcome-oriented**, even if easy to collect. It may independently be **gameable** through superficial links. D14 test flakiness reflects testing-feedback reliability, an **outcome of the verification process**, but still needs an independent assessment of gameability.

## Consequences

No metric or assurance question is added or removed by this clarification. Future metric reviews must score the two criteria independently. Reporting will not mislabel 18 mixed checks as 18 numeric outcome metrics.
