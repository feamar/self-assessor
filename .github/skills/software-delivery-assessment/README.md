# Software Delivery Assessment skill

A read-only, evidence-first GitHub Copilot agent skill for assessing one service's software delivery. It evaluates **30 dimensions**, code and tests separately, and conventional, AI-assisted and AI-driven perspectives.

## Install

Copy this directory to `.github/skills/software-delivery-assessment/` in the repository to assess, or install it in a supported personal skills location. Use an agent host with authorized repository access; external CI, incident and scanner data are optional.

## Start

> Assess this service using the software-delivery-assessment skill. Inspect available evidence first, ask only questions that resolve material gaps, and report the conventional, AI-assisted and AI-driven perspectives.

The assessor does not edit product files or deploy anything. Builds, tests, scanners and external systems require separate approval. Missing evidence stays **unknown**, not a failing score.

## Files

- `SKILL.md`: operational workflow and guardrails
- `references/dimensions.md`: 30 assessment dimensions and scoring anchors
- `references/perspectives.md`: perspective-specific readiness and scoring
- `references/evidence.md`: repository, CI/CD, SRE and external report guidance
- `references/report.md`: concise report and optional detailed ledger

This is an assessment framework, not a compliance certification or preconfigured integration.
