# Initial reporting: three substantial expert assessments

**Mandatory initial deliverable:** three distinct Markdown reports covering **conventional, AI-assisted and AI-driven** delivery, based on the same evidence but independently reasoned. **Target 5–10 printed pages per perspective** where enough defensible material exists. Markdown does not enforce exact pagination: aim for the substance of 5–10 well-laid-out pages, with real observations, explanation and supporting evidence rather than repetitive prose. With limited evidence, write a shorter honest report, clearly describing what could not be established. **Do not save the expert explanation for a later optional report.**

## Document presentation

Start each report with a professional title, perspective, service, revision, assessment date/window and a prominent **short executive judgment**. Reserve a separate **Final verdict** as the final substantive section, with a clearly stated qualitative **Overall score**. Structure the body with clear numbered headings, readable paragraphs, selective tables, explicit evidence links and concise summaries where useful. The executive judgment belongs at the beginning but **does not replace the full analysis**. No compulsory weighted score, maturity heat map or mechanical repetition of all 18 dimensions. Quote factual values with units, time periods, definitions and denominators; never invent numbers, charts or sources. A Markdown report can later be printed/exported, but it should already be useful in source form.

## Required expert content in each initial report

### 1. Executive judgment

Explain candidly how well delivery performs under **this perspective** and why. Highlight proven strengths, largest consequential gaps, overall evidence confidence and highest-priority next direction. Do not print an arbitrary numerical grade by default.

### 2. Service context, boundaries and evidence confidence

Describe the service/user outcome, evaluated repository/revision, deployment/environment boundaries and assessment window. Summarize **what was actually inspected**: CI/CD history, SonarQube or other reports, tests, OpenShift GitOps sync/rollout traces, SLO/incident records, work intake and user results, where available. Distinguish verified evidence, interviews, configuration, missing evidence and out-of-scope sources. Explain how gaps constrain the verdict.

### 3. Actual delivery and user outcomes

**Explicitly examine whether the team has a trustworthy dashboard or accessible recurring report** for our delivery outcome metrics and relevant DORA indicators, not merely whether metrics have ever been discussed. Check dashboard location/access, definitions, source links, data freshness, history/trends and whether results inform decisions. If present, corroborate sample values; if absent or unverified, label the status correctly. **If credible outcome measurement is genuinely missing, argue prominently for an evidence-backed delivery metrics dashboard** using [dashboard guidance](measurement-dashboard.md). The dashboard is a means to learn and improve, not an outcome measure or a score on its own.

Interpret demand-to-user **end-to-end lead time**, genuine production deployment frequency, availability, failures/recovery, first-pass acceptance and user satisfaction or cost where naturally measured. Describe trends and variability, not just snapshots. Don't confuse commit-to-production time with end-to-end lead time; don't treat an empty incident period as proof of rapid recovery. Missing metric definitions or event records must be stated as gaps rather than estimated.

### 4. Engineering, testing, pipeline and operational evidence

Inspect code quality separately from **test effectiveness**; evaluate representative risks, CI/CD execution (not merely YAML), enforced quality/security gates, actual SonarQube findings with report scope, artifact provenance, release/rollback safety and significant non-functional/operations checks. Use only relevant items from the 18-dimension menu. Explain **how each observation relates to a real delivery outcome or risk**, rather than awarding credit for TDD/BDD/automation ceremonies.

### 5. OpenShift and reconciliation evidence where applicable

Consider OpenShift GitOps/Argo CD sync history, reconciliation logs, Flux equivalents, OpenShift rollout history, failed/stuck syncs, retries and drift. Correlate application, environment, namespace, manifest/Git revision, timestamps, pipeline promotion, rollout readiness, runtime health and user impact if records permit. Explicitly distinguish **sync**, **deployment**, **successful release**, and **customer-visible operation**. A green synchronization is **not a measured customer outcome**.

### 6. Full expert interpretation — mandatory in the initial report

This is the heart of the report. Explain **why the observed results, controls and gaps justify the judgment** under the selected conventional, AI-assisted or AI-driven benchmark. Discuss the strength of the evidence and counterevidence. For each major concern: **what happened, which evidence supports it, why it matters to outcomes, what is confirmed versus only plausible, and what would improve it**. Connect observed strengths to reasons for confidence. State what an excellent system would demonstrably show that this one does or does not. Poor outcomes warrant clear criticism; good results deserve specific praise; exceptional sustained results warrant a precise explanation and encouragement to keep doing what works.

### 7. Ranked top 10 improvement factors — mandatory in each report

Produce a clearly numbered **Top 10 improvements**, in descending order of **expected consequence for real delivery outcomes and risk reduction**, using [ranking guidance](improvement-ranking.md). Give each rank a **specific improvement factor**, its supporting evidence or explicitly marked unverified gap, **why it matters**, **recommended action**, and **how to verify progress**. Rank using expert reasoning (impact, evidence, urgency, dependency and feasibility), **not a weighted score or checklist compliance**. The order must be meaningful and perspective-specific, even if some underlying findings overlap.

If reliable delivery measurements/DORA indicators or dashboard visibility are genuinely absent, **a minimal trustworthy metrics collection and dashboard is usually a top-priority improvement**, particularly from the AI-driven perspective. If dashboard existence is simply **not established**, first recommend finding/validating it rather than claiming none exists. Distinguish an observed weakness from an investigation needed to resolve uncertainty. **Aim for exactly ten meaningful items**, but if fewer than ten can be supported, state that openly; **never fabricate problems, generic filler or mandatory work** to reach the number. When delivery is excellent, justified ongoing investment and maintenance opportunities may be included, clearly distinguished from defects.

### 8. Evidence references and unresolved questions

Provide concise traceable anchors: dated deployment/run IDs, SonarQube report revision/scope, OpenShift sync and rollout record, incident metrics, code locations and meaningful interview qualifications. Make high-impact evidence gaps explicit, including what additional information a team lead could supply. Exclude credentials, tokens and protected production payloads.

### 9. Final verdict — required last section

**Every report must end in an unmistakable concluding verdict**. Give a one-sentence professional conclusion, followed by an explicit, non-numeric qualitative rating:

> **Final verdict:** Delivery is progressing and has clear strengths, but significant improvements to evidence and release reliability remain necessary. **Overall score: Satisfactory.**

This is an **illustrative format, not a default or presumed assessment**. Choose the label warranted by this perspective's evidence: **Excellent**, **Good**, **Satisfactory**, **Needs improvement**, **Unsatisfactory**, or **Not demonstrated (insufficient evidence)**. Explain exactly why this label fits and what single change or strength is decisive. Distinguish **unproven quality** from **proven poor quality**. If data is missing, do not claim Satisfactory merely to be pleasant. These are **qualitative judgments**, not numerical totals, bands calculated from the 18 dimensions, or a resurrection of weighted scoring. Apply [evidence calibration](perspectives.md). The final verdict must not be buried in the executive summary or omitted because an opening judgment exists.

## Shared evidence, distinct viewpoints

All three reports must have **full expert reasoning** rather than a single short paragraph with the perspective name swapped. Reuse common source references accurately, but change the expected standards, causal interpretation and recommendations as appropriate. Conventional judges human-led Google/SRE-grade engineering, AI-assisted demands more leverage and verification, and AI-driven demands the strongest measured outcomes and independently controlled agents.

## Delivery and post-report options

Create three distinct, non-destructively named Markdown artifacts (e.g. `assessment-conventional.md`, `assessment-ai-assisted.md`, `assessment-ai-driven.md`, optionally under a dated run folder). **Show the complete user-selected report** (default conventional) and make the other two accessible without rerunning.

**Only afterward**, the developer may request (1) a deeper **technical implementation appendix** for team leads or (2) instructions/SKILL.md files for future agents. These are **independent optional follow-ups**. The initial reports must not omit expert reasons or material concerns awaiting the appendix. Writing to the assessed product repository needs approval; if absent, provide separate copy-ready files and state where they were and were not saved.

**Pre-delivery check:** Confirm **each of the three** reports has a traceable measurement/dashboard conclusion, a genuinely ranked improvement section (target ten evidence-supported factors), and the **Final verdict / Overall score** at the end. An executive summary alone does not satisfy the concluding verdict.
