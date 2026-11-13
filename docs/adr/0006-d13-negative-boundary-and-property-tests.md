# ADR 0006: Retire D13 — Negative, boundary and property tests

**Status:** Accepted  
**Original dimension:** D13 — Negative, boundary and property tests  
**Disposition:** Retired

## Context

Enumerating a complete failure-mode denominator is difficult; inspect consequential failure paths only as part of test effectiveness.

## Decision

Remove this as a standalone assessed dimension. Inspect relevant boundary/negative cases within D12 when risk warrants it; no separate denominator.

## Consequences

The assessor does not score the former metric or request its collection by default. Relevant evidence may still be used to explain measured outcomes or assess a material risk. This decision can be revisited if a simpler, transparent outcome metric is identified.
