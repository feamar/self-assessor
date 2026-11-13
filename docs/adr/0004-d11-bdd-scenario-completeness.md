# ADR 0004: Retire D11 — BDD scenario completeness

**Status:** Accepted  
**Original dimension:** D11 — BDD scenario completeness  
**Disposition:** Retired

## Context

Scenario counts reward documentation activity; assess whether tests meaningfully catch incorrect accepted behavior.

## Decision

Remove this as a standalone assessed dimension. Inspect critical acceptance behavior under D12; BDD artifacts may be evidence, not a result.

## Consequences

The assessor does not score the former metric or request its collection by default. Relevant evidence may still be used to explain measured outcomes or assess a material risk. This decision can be revisited if a simpler, transparent outcome metric is identified.
