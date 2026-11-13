# Self Assessor

An evidence-first software delivery quality assessment skill for GitHub Copilot and compatible coding agents.

## Install

Copy [the skill folder](.github/skills/software-delivery-assessment/) into your target repository at `.github/skills/software-delivery-assessment/` (or a supported personal skills location).

## Run

Ask your agent: **“Assess this service using the software-delivery-assessment skill. Inspect evidence first, ask only targeted questions about gaps, and report conventional, AI-assisted and AI-driven perspectives.”**

The skill evaluates 30 dimensions and separately reviews code and test quality. It is read-only by default; external systems and test execution require approval. Missing evidence is marked unknown rather than scored as failure.

See [SKILL.md](.github/skills/software-delivery-assessment/SKILL.md) and [the skill README](.github/skills/software-delivery-assessment/README.md).