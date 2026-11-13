# Initial reporting: three substantial expert assessments

**Mandatory initial deliverable:** three distinct Markdown reports covering **conventional, AI-assisted and AI-driven** delivery, based on the same evidence but independently reasoned. **Target 5–10 printed pages per perspective** where enough defensible material exists. Markdown does not enforce exact pagination: aim for the substance of 5–10 well-laid-out pages, with real observations, explanation and supporting evidence rather than repetitive prose. With limited evidence, write a shorter honest report, clearly describing what could not be established. **Do not save the expert explanation for a later optional report.**

## Document presentation

Start each report with a professional title, perspective, service, revision, assessment date/window and a prominent **short executive judgment**. Structure the body with clear numbered headings, readable paragraphs, selective tables, explicit evidence links and concise summaries where useful. The executive judgment belongs at the beginning but **does not replace the full analysis**. No compulsory weighted score, maturity heat map or mechanical repetition of all 18 dimensions. Quote factual values with units, time periods, definitions and denominators; never invent numbers, charts or sources. A Markdown report can later be printed/exported, but it should already be useful in source form.

## Required expert content in each initial report

### 1. Executive judgment

Explain candidly how well delivery performs under **this perspective** and why. Highlight proven strengths, largest consequential gaps, overall evidence confidence and highest-priority next direction. Do not print an arbitrary numerical grade by default.

### 2. Service context, boundaries and evidence confidence

Describe the service/user outcome, evaluated repository/revision, deployment/environment boundaries and assessment window. Summarize **what was actually inspected**: CI/CD history, SonarQube or other reports, tests, OpenShift GitOps sync/rollout traces, SLO/incident records, work intake and user results, where available. Distinguish verified evidence, interviews, configuration, missing evidence and out-of-scope sources. Explain how gaps constrain the verdict.

### 3. Actual delivery and user outcomes

Interpret demand-to-user **end-to-end lead time**, genuine production deployment frequency, availability, failures/recovery, first-pass acceptance and user satisfaction or cost where naturally measured. Describe trends and variability, not just snapshots. Don't confuse commit-to-production time with end-to-end lead time; don't treat an empty incident period as proof of rapid recovery. Missing metric definitions or event records must be stated as gaps rather than estimated.

### 4. Engineering, testing, pipeline and operational evidence

Inspect code quality separately from **test effectiveness**; evaluate representative risks, CI/CD execution (not merely YAML), enforced quality/security gates, actual SonarQube findings with report scope, artifact provenance, release/rollback safety and significant non-functional/operations checks. Use only relevant items from the 18-dimension menu. Explain **how each observation relates to a real delivery outcome or risk**, rather than awarding credit for TDD/BDD/automation ceremonies.

### 5. OpenShift and reconciliation evidence where applicable

Consider OpenShift GitOps/Argo CD sync history, reconciliation logs, Flux equivalents, OpenShift rollout history, failed/stuck syncs, retries and drift. Correlate application, environment, namespace, manifest/Git revision, timestamps, pipeline promotion, rollout readiness, runtime health and user impact if records permit. Explicitly distinguish **sync**, **deployment**, **successful release**, and **customer-visible operation**. A green synchronization is **not a measured customer outcome**.

### 6. Full expert interpretation — mandatory in the initial report

This is the heart of the report. Explain **why the observed results, controls and gaps justify the judgment** under the selected conventional, AI-assisted or AI-driven benchmark. Discuss the strength of the evidence and counterevidence. For each major concern: **what happened, which evidence supports it, why it matters to outcomes, what is confirmed versus only plausible, and what would improve it**. Connect observed strengths to reasons for confidence. State what an excellent system would demonstrably show that this one does or does not. Poor outcomes warrant clear criticism; good results deserve specific praise; exceptional sustained results warrant a precise explanation and encouragement to keep doing what works.

### 7. Prioritized improvements and verification

Recommend a small number of meaningful changes with **why**, expected consequence, useful sequencing and **how to verify improvement** from actual delivery measurements or effective safety controls. If results are excellent, preserve successful approaches and name truly optional future gains only when justified. No forced backlog, no invented owner, no automatic agent skill generation.

### 8. Evidence references and unresolved questions

Provide concise traceable anchors: dated deployment/run IDs, SonarQube report revision/scope, OpenShift sync and rollout record, incident metrics, code locations and meaningful interview qualifications. Make high-impact evidence gaps explicit, including what additional information a team lead could supply. Exclude credentials, tokens and protected production payloads.

## Shared evidence, distinct viewpoints

All three reports must have **full expert reasoning** rather than a single short paragraph with the perspective name swapped. Reuse common source references accurately, but change the expected standards, causal interpretation and recommendations as appropriate. Conventional judges human-led Google/SRE-grade engineering, AI-assisted demands more leverage and verification, and AI-driven demands the strongest measured outcomes and independently controlled agents.

## Delivery and post-report options

Create three distinct, non-destructively named Markdown artifacts (e.g. `assessment-conventional.md`, `assessment-ai-assisted.md`, `assessment-ai-driven.md`, optionally under a dated run folder). **Show the complete user-selected report** (default conventional) and make the other two accessible without rerunning.

**Only afterward**, the developer may request (1) a deeper **technical implementation appendix** for team leads or (2) instructions/SKILL.md files for future agents. These are **independent optional follow-ups**. The initial reports must not omit expert reasons or material concerns awaiting the appendix. Writing to the assessed product repository needs approval; if absent, provide separate copy-ready files and state where they were and were not saved.
