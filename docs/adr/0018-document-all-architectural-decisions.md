# ADR-0018: Document every accepted architectural decision

**Status:** Accepted

## Context

The assessment model is evolving. Without an audit trail, the rationale for introducing, modifying or retiring metrics and checks can be lost.

## Decision

Document **every accepted architectural decision** in an ADR even when not explicitly requested. This includes changes to metrics, definitions, strength criteria, retained exceptions, assessment dimensions, perspectives, scoring, workflows, assurance boundaries and the ADR policy.

Each ADR briefly captures the context, decision, rationale and consequences. Commit it alongside the architectural change and index it in `docs/adr/README.md`. If a decision is superseded, preserve its historical ADR and link to the new decision.

Exploratory evaluations, unaccepted proposals, typo fixes and purely editorial changes are not architectural decisions and need no ADR.

## Consequences

The repository is the authoritative audit trail of accepted design changes. ADRs are maintainer records, not mandatory input to the assessment agent. This requirement applies to future decisions rather than retroactively to every conversation.
