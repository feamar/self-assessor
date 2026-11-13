# ADR-0026: Start Self Assessor from a GitHub URL in Copilot

**Status:** Accepted — active

## Context

A lead developer should launch the assessment from their workstation, with their **product repository open**, by giving Copilot one unambiguous prompt:

```text
Start https://github.com/feamar/self-assessor/
```

The assessment framework lives in a different GitHub repository. Native Copilot agent-skill discovery normally scans recognized project or personal skill directories, **not arbitrary repository URLs**. VS Code Copilot Agent mode can fetch remote URLs (sometimes requiring explicit `#fetch` and approval), but URL retrieval **is not native skill installation**. Without a clear bootstrap Copilot could read only the README, start assessing `self-assessor` instead of the user's project, or falsely claim instructions were loaded.

## Decision

Make the root repository URL the **preferred conversational entrypoint** by providing a prominent executable `Start` example and an agent-readable root `START.md`. On URL retrieval the agent must fetch the complete `.github/skills/software-delivery-assessment/SKILL.md`, its referenced guidance and relevant evidence, then assess the **currently open service workspace**. It must never silently substitute this instruction repository as the target.

Produce all three perspectives as separate Markdown outcomes, display the user's selected perspective (conventional by default) and preserve permissions: inspect read-only by default, do not overwrite outcomes or run tools without relevant authorization.

Where an agent cannot fetch the remote URL, **fail clearly rather than pretending to have loaded the skill**. Provide a URL-fetch fallback using `#fetch` in VS Code and a documented **native installation fallback** using `gh skill preview` / `gh skill install ... --scope user` (GitHub CLI 2.90.0+), preserving isolation from the assessed repository. Use the existing conventional Copilot skill directory layout for installed skills. Include light workspace-local guidance in `.github/copilot-instructions.md` and `AGENTS.md` for developers who open the instructions repository itself.

## Consequences

The usual start is one line and does not require manually copying the skill into a product repository **when remote access is available**. Support remains conditional on the Copilot host's retrieval permissions and the developer's open workspace. Native skill activation and universal one-line URL behavior across all Copilot clients **cannot be guaranteed by repository files**; use the tested native install mechanism when necessary. A future smoke test should validate the actual host's URL retrieval and three-outcome workflow.

The root README and START.md are operational entrypoints; this ADR records the design decision, while the existing skill and ADRs 0023–0025 continue to govern assessment content and reporting.

**Clarified by [ADR-0027](0027-high-reasoning-preflight-both-ides.md):** the developer may use **Microsoft Visual Studio or VS Code**, and both require a High-reasoning startup check before the assessment. VS Code's `#fetch` mechanism is not assumed to exist in Visual Studio.
