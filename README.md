# Self Assessor

**Start a software delivery assessment from a lead developer's workstation.** Open the **service or product repository to assess** in **Microsoft Visual Studio or Visual Studio Code** with GitHub Copilot **Agent mode**, then enter exactly:

```text
Start https://github.com/feamar/self-assessor/
```

**Copilot agent reading this page:** Treat the URL as the *assessment instructions*, **not** as the codebase being assessed. Fetch and follow **[START.md](https://github.com/feamar/self-assessor/blob/main/START.md)**, which loads the complete [Software Delivery Assessment skill](.github/skills/software-delivery-assessment/SKILL.md) and its references. Start against the **developer's open workspace**, not this repository. If the URL or required files cannot be fetched, **do not pretend the assessment started**; use the fallback below.

## Before the assessment: High reasoning

This expert judgment is a complex task. **High thinking/reasoning effort (or higher) is required** with a compatible Copilot model. The startup instructions tell Copilot to check the *actual selected chat model's* thinking-effort setting. If an exposed, authorized IDE control can set it to High, Copilot should do so and verify. Otherwise it must **ask the developer to select High and confirm before assessment begins**; it must not claim to inspect or change hidden UI settings.

- **Visual Studio 2026 (18.9+):** Copilot Chat → **Model picker → Manage models** → choose a supported model → set **Thinking effort: High**.
- **VS Code:** Copilot Chat → **Model picker** → choose a supported reasoning model → open its **configuration submenu** (arrow beside the model) → select **High**.

If the selected model or host does not offer High, select a compatible model where available; otherwise ask the developer whether to continue with an explicit exception. See [Visual Studio model options](https://learn.microsoft.com/en-us/visualstudio/ide/copilot-usage-and-models?view=visualstudio) and [VS Code thinking effort](https://code.visualstudio.com/docs/agent-customization/language-models).

## What happens after Start

After the High-effort preflight, Copilot loads the full assessment instructions, inspects the current workspace, **asks where to find CI/CD runs, SonarQube, OpenShift synchronization history and other meaningful evidence**, including an open-ended request for any further sources. It inspects approved historical evidence and assesses **all three perspectives**. The initial output is three **well-formatted 5–10-page expert reports** including the analysis, concerns, rationale and recommendations. It displays conventional by default (or the user's selection); a deeper technical appendix is optional afterward. Drafting instructions for future agents is another, separate optional follow-up. It does not change product code or silently write to the assessed repository.

This project is a source of **read-only assessment instructions**, not the assessment target. Merely saying `Start` does not authorize executing scripts, changing files or accessing restricted services. Copilot may ask permission for external URLs or other tools.

## If a bare URL does not load

Some Copilot hosts do not automatically retrieve arbitrary repository URLs. **In VS Code**, try explicitly fetching the bootstrap document:

```text
Start #fetch https://raw.githubusercontent.com/feamar/self-assessor/main/START.md
```

**In Visual Studio**, if the URL does not load, open [START.md](START.md) in a browser and supply its text to Copilot Chat, or install/copy the skill to a supported personal or workspace skills directory. **For native skill discovery**, GitHub CLI 2.90.0+ also supports installing this public skill to the developer's personal skill location (rather than changing the assessed repository):

```sh
gh skill preview feamar/self-assessor software-delivery-assessment
gh skill install feamar/self-assessor software-delivery-assessment --scope user
```

Then start a new Copilot session (or use `/skills reload` in Copilot CLI) and request: `Run the software-delivery-assessment skill on this workspace; show conventional.` The direct URL is the preferred entry point; installation is a fallback, **not an automatic side effect of Start**. See [VS Code web context](https://code.visualstudio.com/docs/chat/copilot-chat-context), [Visual Studio skills](https://learn.microsoft.com/en-us/visualstudio/ide/copilot-agent-skills?view=visualstudio) and [GitHub skill installation](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/add-skills).

## Repository contents

- [START.md](START.md) — remote bootstrap instructions for Copilot
- [SKILL.md](.github/skills/software-delivery-assessment/SKILL.md) — assessment workflow
- [References](.github/skills/software-delivery-assessment/README.md) — metrics, evidence, perspectives, report and agent improvement guidance
- [ADRs: active and inactive](docs/adr/README.md) — why the framework is designed this way
- [ADR-0000: original 30 dimensions](docs/adr/0000-original-assessment-rationale.md) — historical rationale

Architecture decisions are recorded in ADRs alongside changes. Outcome files and agent improvement skills must be kept separate from the assessment instructions. Missing evidence stays **unknown**, not failure.
