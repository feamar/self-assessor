# Self Assessor

**Start a software delivery assessment from a lead developer's workstation.** Open the **service or product repository to assess** in VS Code with GitHub Copilot **Agent mode**, then enter exactly:

```text
Start https://github.com/feamar/self-assessor/
```

**Copilot agent reading this page:** Treat the URL as the *assessment instructions*, **not** as the codebase being assessed. Fetch and follow **[START.md](https://github.com/feamar/self-assessor/blob/main/START.md)**, which loads the complete [Software Delivery Assessment skill](.github/skills/software-delivery-assessment/SKILL.md) and its references. Start against the **developer's open workspace**, not this repository. If the URL or required files cannot be fetched, **do not pretend the assessment started**; use the fallback below.

## What happens after Start

Copilot loads the full assessment instructions, inspects the current workspace and available approved evidence, asks only essential scope or access questions, and assesses **all three perspectives**: conventional, AI-assisted and AI-driven. It prepares three separate concise Markdown outcomes, **displays conventional by default** (or the user's chosen perspective), and proposes agent-ready improvement skills when findings justify them. It does not change product code or silently write to the assessed repository.

This project is a source of **read-only assessment instructions**, not the assessment target. Merely saying `Start` does not authorize executing scripts, changing files or accessing restricted services. Copilot may ask permission for external URLs or other tools.

## If a bare URL does not load

Some Copilot hosts do not automatically retrieve arbitrary repository URLs. In VS Code, try explicitly fetching the bootstrap document:

```text
Start #fetch https://raw.githubusercontent.com/feamar/self-assessor/main/START.md
```

For **native skill discovery**, GitHub CLI 2.90.0+ supports installing this public skill to the developer's personal skill location (rather than changing the assessed repository):

```sh
gh skill preview feamar/self-assessor software-delivery-assessment
gh skill install feamar/self-assessor software-delivery-assessment --scope user
```

Then start a new Copilot session (or use `/skills reload` in Copilot CLI) and request: `Run the software-delivery-assessment skill on this workspace; show conventional.` The direct URL is the preferred entry point; installation is a fallback, **not an automatic side effect of Start**. See [VS Code web context](https://code.visualstudio.com/docs/chat/copilot-chat-context) and [GitHub skill installation](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/add-skills).

## Repository contents

- [START.md](START.md) — remote bootstrap instructions for Copilot
- [SKILL.md](.github/skills/software-delivery-assessment/SKILL.md) — assessment workflow
- [References](.github/skills/software-delivery-assessment/README.md) — metrics, evidence, perspectives, report and agent improvement guidance
- [ADRs: active and inactive](docs/adr/README.md) — why the framework is designed this way
- [ADR-0000: original 30 dimensions](docs/adr/0000-original-assessment-rationale.md) — historical rationale

Architecture decisions are recorded in ADRs alongside changes. Outcome files and agent improvement skills must be kept separate from the assessment instructions. Missing evidence stays **unknown**, not failure.
