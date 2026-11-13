# ADR 0010: Retire D21 — Exceptions and ADR audit trail

**Status:** Accepted  
**Original dimension:** D21 — Exceptions and ADR audit trail  
**Disposition:** Retired

## Context

ADR counts reward process documentation, not delivery results; request decision evidence only for material risks or exceptions.

## Decision

Remove this as a standalone assessed dimension. Request decisions and exception rationale only for material security, architecture or delivery risks; do not score ADR production.

## Consequences

The assessor does not score the former metric or request its collection by default. Relevant evidence may still be used to explain measured outcomes or assess a material risk. This decision can be revisited if a simpler, transparent outcome metric is identified.
