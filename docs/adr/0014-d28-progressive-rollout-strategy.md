# ADR 0014: Retire D28 — Progressive rollout strategy

**Status:** Accepted  
**Original dimension:** D28 — Progressive rollout strategy  
**Disposition:** Retired

## Context

Canary/flag adoption rates are practice metrics, not universal outcomes; assess release safety through actual recovery and safeguards.

## Decision

Remove this as a standalone assessed dimension. Verify recovery, migration safety and production health under D08; rollout technique is a possible implementation, not a goal.

## Consequences

The assessor does not score the former metric or request its collection by default. Relevant evidence may still be used to explain measured outcomes or assess a material risk. This decision can be revisited if a simpler, transparent outcome metric is identified.
