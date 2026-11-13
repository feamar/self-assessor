# Software Delivery Assessment skill

An evidence-first GitHub Copilot agent skill that delivers a **concise qualitative verdict** for one selected **conventional, AI-assisted or AI-driven** perspective. Strong delivery outcomes, critical controls and expert judgment replace arbitrary numeric weights.

## Use

Copy this folder to `.github/skills/software-delivery-assessment/` in the target repository (or supported personal skills location), then ask:

> Assess this service from the AI-driven perspective in three short paragraphs and prepare agent-ready skills for consequential improvements.

Default perspective: conventional. Main report: **three paragraphs maximum / one sheet**, readable by lead developers and CTOs. A numerical grade is optional only on explicit request; the private 0–10 calibration requires strong evidence for high grades. AI-driven missing outcome data calls for a measurement skill.

- `SKILL.md` — workflow and safeguards
- `references/perspectives.md` — perspective standards and calibration
- `references/report.md` — leadership report format
- `references/remediation-skills.md` — executable improvement skills as separate artifacts
- `references/metrics.md`, `dimensions.md`, `evidence.md` — measurement and evidence support

Read-only by default. Accessing external systems, running tests, writing skill files and changing product code require permission. Architectural decisions are logged in `docs/adr/` as maintainer history.
