# ADR-0022: Draft agent skills for evidenced improvements

**Status:** Superseded / inactive — see [ADR-0028](0028-evidence-first-report-before-optional-agent-skills.md)

## Context

Copilot agents can carry out bounded quality and delivery improvements, but generic recommendations are not directly executable.

## Decision

For one to three important agent-addressable findings, draft **complete single-purpose GitHub Copilot SKILL.md files** with scope, evidence, steps, permissions, independent acceptance checks and safeguards. Keep them outside the leadership report. For AI-driven delivery missing outcomes, prioritize rigorous measurement/instrumentation of real results.

Do not write skill files to the assessed repository without explicit permission, or execute their product changes merely because they were drafted. No self-approval, uncontrolled access or deployment.

## Consequences

Findings translate into independently verifiable tasks without compromising the read-only assessment or report brevity.

**Historical note:** [ADR-0028](0028-evidence-first-report-before-optional-agent-skills.md) supersedes the default skill-generation step. Future agent instructions are **offered only after reports** and drafted solely when explicitly requested.
