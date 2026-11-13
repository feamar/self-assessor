# Software Delivery Assessment skill

An evidence-first Copilot skill for **Visual Studio or VS Code**, requiring **High reasoning effort or an explicit exception before assessment**, that **first seeks CI/CD, SonarQube, test, operational and applicable OpenShift synchronization/rollout evidence**, then evaluates all three perspectives and produces **three substantial 5–10-page Markdown expert reports**, each with an evidence-based **top ten ranked improvements**, a check of **delivery/DORA metrics and dashboard**, and a **final qualitative Overall score**, displaying the user's choice. The initial reports include the full reasoning and material concerns. A deeper technical appendix is optional. Critical, evidence-specific feedback replaces vague encouragement and arbitrary scores.

## Use

**Preferred:** With the product repository open in **Visual Studio or VS Code** GitHub Copilot Agent mode, type `Start https://github.com/feamar/self-assessor/`. The repository root [START.md](../../../START.md) bootstraps the full skill through remote files; it is not native automatic skill discovery and depends on the Copilot host's URL-fetch capability. If that fails, use the host-specific fallback (`#fetch` in VS Code; supplying START.md or installing the skill in Visual Studio) documented in the [root README](../../../README.md).

**Alternatively**, install this skill to a recognized project/personal skills location and ask:

> Assess this service. Ask where CI/CD history, SonarQube, OpenShift synchronization logs and other relevant evidence can be found. Ask whether further sources exist. Produce three detailed expert perspective reports, showing conventional.

**Evidence collection is the priority.** Prompt the developer for relevant missing pipeline/report sources, inspect historical runs and outcomes, and be transparent about gaps. All three perspectives are assessed from the same evidence. **Each initial report targets 5–10 printed pages of substantive explanation**, for lead developers and CTOs. The selected one is shown; the other two remain available as files. Weak delivery gets clear corrections, good delivery receives earned praise and next steps, and genuinely excellent delivery receives explicit evidence-based recognition. Numeric grades are optional on request.

- `SKILL.md` — workflow and safeguards
- `references/perspectives.md` — perspective standards and calibration
- `references/report.md` — initial 5–10-page expert perspective reports and required final verdict
- `references/measurement-dashboard.md` — outcome/DORA measurement and dashboard recommendations
- `references/improvement-ranking.md` — reasoned top-ten improvement prioritization
- `references/team-lead-report.md` — **optional, post-assessment technical implementation appendix**
- `references/remediation-skills.md` — **optional, only after the report and the developer's opt-in**
- `references/metrics.md`, `dimensions.md`, `evidence.md` — measurement and evidence support

**Only after presenting the full expert reports**, optionally offer a deeper technical appendix for team leads. Agent instructions are an **independent** optional follow-up; do not prepare either in advance. Read-only by default. If writing assessment results to the target repository is not authorized, provide three separate Markdown artifacts instead. External access, running tests, writing files and changing product code require permission. Architectural decisions are logged in `docs/adr/` as maintainer history.
