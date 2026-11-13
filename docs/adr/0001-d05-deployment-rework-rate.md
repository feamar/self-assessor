# ADR 0001: Retire D05 — Deployment rework rate

**Status:** Accepted  
**Original dimension:** D05 — Deployment rework rate  
**Disposition:** Retired

## Context

Rework attribution is not naturally obvious; first-pass acceptance yield is the preferred result metric when genuine acceptance events exist.

## Decision

Remove this as a standalone assessed dimension. Use first-pass acceptance yield only where acceptance is naturally recorded; otherwise use end-to-end lead time and a targeted question about rework.

## Consequences

The assessor does not score the former metric or request its collection by default. Relevant evidence may still be used to explain measured outcomes or assess a material risk. This decision can be revisited if a simpler, transparent outcome metric is identified.
