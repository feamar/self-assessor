# Self Assessor

A concise, evidence-first [software delivery assessment skill](.github/skills/software-delivery-assessment/SKILL.md) for GitHub Copilot and compatible coding agents.

It starts with **real delivery outcomes**, investigates meaningful gaps and verifies critical controls. It **evaluates conventional, AI-assisted and AI-driven delivery in every run**, produces **three separate evidence-based Markdown judgments**, and shows the **user-selected perspective** (conventional by default). It praises demonstrated excellence, gives candid corrective feedback on weaker performance, and drafts separate agent-ready improvement skills.

## Use

Copy `.github/skills/software-delivery-assessment/` to your target repository or a supported personal skills folder. Ask the agent to assess delivery outcomes first and ask only questions that resolve important gaps.

- [Skill instructions](.github/skills/software-delivery-assessment/SKILL.md)
- [Metric definitions](.github/skills/software-delivery-assessment/references/metrics.md)
- [Active checks](.github/skills/software-delivery-assessment/references/dimensions.md)
- [Architecture decision records — active and inactive](docs/adr/README.md)
- [Where the assessment began (ADR-000)](docs/adr/000-original-assessment-rationale.md)

The skill operates read-only unless additional permissions are granted. Missing measurements remain unknown.

## Architecture decision policy

Every accepted architectural change must include a corresponding [ADR](docs/adr/README.md) in the same commit; exploratory discussions and editorial changes do not require one.
