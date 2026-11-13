# Software Delivery Assessment skill

An evidence-first Copilot skill for **Visual Studio or VS Code**, requiring **High reasoning effort or an explicit exception before assessment**, that **evaluates all three perspectives in every run**, prepares **three separate Markdown judgments** and **displays the perspective chosen by the user** (conventional by default). Critical, evidence-specific feedback replaces vague encouragement and arbitrary scores.

## Use

**Preferred:** With the product repository open in **Visual Studio or VS Code** GitHub Copilot Agent mode, type `Start https://github.com/feamar/self-assessor/`. The repository root [START.md](../../../START.md) bootstraps the full skill through remote files; it is not native automatic skill discovery and depends on the Copilot host's URL-fetch capability. If that fails, use the host-specific fallback (`#fetch` in VS Code; supplying START.md or installing the skill in Visual Studio) documented in the [root README](../../../README.md).

**Alternatively**, install this skill to a recognized project/personal skills location and ask:

> Assess this service from the AI-driven perspective in three short paragraphs and prepare agent-ready skills for consequential improvements.

All three perspectives are assessed from the same evidence. **Each outcome is at most three paragraphs / one page**, for lead developers and CTOs. The selected one is shown; the other two remain available as files. Weak delivery gets clear corrections, good delivery receives earned praise and next steps, and genuinely excellent delivery receives explicit evidence-based recognition. Numeric grades are optional on request.

- `SKILL.md` — workflow and safeguards
- `references/perspectives.md` — perspective standards and calibration
- `references/report.md` — leadership report format
- `references/remediation-skills.md` — executable improvement skills as separate artifacts
- `references/metrics.md`, `dimensions.md`, `evidence.md` — measurement and evidence support

Read-only by default. If writing assessment results to the target repository is not authorized, provide three separate Markdown artifacts instead. External access, running tests, writing files and changing product code require permission. Architectural decisions are logged in `docs/adr/` as maintainer history.
