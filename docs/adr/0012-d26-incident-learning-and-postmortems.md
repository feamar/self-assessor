# ADR 0012: Retire D26 — Incident learning and postmortems

**Status:** Accepted  
**Original dimension:** D26 — Incident learning and postmortems  
**Disposition:** Retired

## Context

Root-cause recurrence rate needs subjective classification; investigate incident learning only when recovery or reliability evidence warrants it.

## Decision

Remove this as a standalone assessed dimension. If significant incidents occurred, ask which remediation actions were verified; don't compute recurrence rate.

## Consequences

The assessor does not score the former metric or request its collection by default. Relevant evidence may still be used to explain measured outcomes or assess a material risk. This decision can be revisited if a simpler, transparent outcome metric is identified.
