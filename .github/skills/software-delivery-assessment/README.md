# Software Delivery Assessment skill

An evidence-first GitHub Copilot skill assessing software delivery through **strong outcomes, targeted diagnostics and essential assurance**, with conventional, AI-assisted and AI-driven perspectives. No maturity-score average or mandatory list of 30 process dimensions.

## Install and use

Copy this directory to `.github/skills/software-delivery-assessment/` in the target repository (or a supported personal skills location), then ask:

> Assess this service using software-delivery-assessment. Start with delivery outcomes, investigate only useful gaps, and report the three perspectives.

The agent is read-only by default; tests, scanners and external access require approval. Unknown evidence does not count as failure.

- `SKILL.md`: short workflow and safeguards
- `references/metrics.md`: strong metric definitions and selection
- `references/dimensions.md`: 18 surviving measurement/assurance prompts
- `references/evidence.md`: sources and interview rules
- `references/perspectives.md`: conventional / AI-assisted / AI-driven
- `references/report.md`: concise decision-ready report

The retired/reframed dimensions have individual decision records in the repository's `docs/adr/` directory. These are audit history, **not required agent context**.
