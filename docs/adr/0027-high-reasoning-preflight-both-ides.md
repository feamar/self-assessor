# ADR-0027: Require High thinking effort in Visual Studio or VS Code

**Status:** Accepted — active  
**Clarifies:** [ADR-0026](0026-remote-url-bootstrap.md)

## Context

The assessment is an evidence-intensive expert judgment run from a lead developer's GitHub Copilot session. The IDE may be **Microsoft Visual Studio or Visual Studio Code**, and their model-picker controls are different. A Copilot agent cannot be assumed to inspect or modify the host IDE's selected thinking effort. Claiming to have forced High in an inaccessible UI would undermine transparency.

## Decision

Before examining the target codebase or performing the assessment, perform a **High thinking-effort preflight** on the **actual chat model**. If High or higher is visibly selected, continue. If a supported host control is actually available to the agent, set High and verify. If the setting is not visible, is lower or is not programmatically changeable, **ask the developer to select High and confirm before proceeding**. Do not silently assume High; do not invent tool APIs or modify undocumented settings.

Guide the user according to their actual host:
- **Visual Studio 2026 v18.9+**: Copilot Chat → Model picker → Manage models → select a compatible reasoning model → choose High.
- **VS Code**: Copilot Chat → Model picker → select a compatible reasoning model → open its configuration/effort submenu → choose High.

When the selected model or host has no High option, offer a compatible reasoning model where available. If that is impossible, **request explicit approval for an exception** rather than blocking indefinitely or continuing silently. A user confirmation can satisfy the preflight but must not be misrepresented as independently machine-verified. The requirement also applies to native locally installed skill activation, not just URL bootstrap.

## Consequences

The recommended single-line entrypoint stays unchanged: `Start https://github.com/feamar/self-assessor/`. An additional preflight conversation may be required. Supported IDEs remain Visual Studio and VS Code; neither programmatic effort control nor universal URL retrieval is guaranteed. The assessment's existing evidence and permissions requirements are unchanged.
