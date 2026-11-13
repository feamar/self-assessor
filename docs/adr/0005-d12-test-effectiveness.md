# ADR 0005: Reframe D12 — Test effectiveness

**Status:** Accepted  
**Original dimension:** D12 — Test effectiveness  
**Disposition:** Reframed

## Context

Mutation-detection rate is specialist-dependent and may reward synthetic mutant performance; retain an evidence question about catching representative real faults.

## Decision

Discard the proposed numerical metric while keeping the underlying risk as an evidence-based assurance question. Retain D12 as the question: do tests demonstrably detect representative meaningful defects? Use authorized execution only.

## Consequences

The assessor does not score the former metric or request its collection by default. Relevant evidence may still be used to explain measured outcomes or assess a material risk. This decision can be revisited if a simpler, transparent outcome metric is identified.
