# ADR 0008: Reframe D17 — Secure coding conformance

**Status:** Accepted  
**Original dimension:** D17 — Secure coding conformance  
**Disposition:** Reframed

## Context

Counting security findings 'prevented' requires an unobservable counterfactual; retain verification of effective critical security controls.

## Decision

Discard the proposed numerical metric while keeping the underlying risk as an evidence-based assurance question. Retain D17 as an assurance check for actual security gates, unresolved critical findings and bypasses.

## Consequences

The assessor does not score the former metric or request its collection by default. Relevant evidence may still be used to explain measured outcomes or assess a material risk. This decision can be revisited if a simpler, transparent outcome metric is identified.
