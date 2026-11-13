# Optional post-report agent improvement skills

**This reference is not part of the default assessment workflow.** The assessor must **first gather available evidence and finish all three perspective reports**. Only **after showing the selected report and obtaining the developer's explicit opt-in** may it draft any agent instructions or SKILL.md files.

When invited, write **complete, focused SKILL.md artifacts**, not vague suggestions, for evidenced high-value improvements. Keep them **separate from the three perspective outcome files**. Consolidate overlapping findings into at most 1–3 independent tasks across the assessment. For excellent delivery without meaningful deficiencies, do not invent remedial tasks.

For each task, draft `.github/skills/<short-task-name>/SKILL.md` with valid `name` and `description` frontmatter, then:

1. **Goal and evidence:** a real observed weakness, source references and intended better result.
2. **Scope and permissions:** relevant service, code paths or systems (where known), missing facts to verify, required access and explicit exclusions.
3. **Bounded steps:** inspect → plan → change/test **only with permission** → independently verify. Favor strong output metrics over process compliance.
4. **Acceptance criteria:** observable success, tests or independent monitoring, relevant before-and-after baseline and human acceptance.
5. **Safety:** no self-approval, gate bypass, secrets, uncontrolled external actions, destructive changes or production deployment; escalate decisions beyond scope.

**If AI-driven outcome evidence is missing and the developer opts in after the report**, prioritize a measurement skill: define intake and user-available delivery events, real production releases, user-impacting incidents and restoration, availability, delivered quality and relevant delivery/agent cost; source each timestamp/event; specify units, denominators, validation, baseline, trends, dashboard and cadence. Do not invent historical records.

**Permission boundary:** Draft complete copy-ready skill files as separate assessment artifacts. **Saving files to a target repository requires explicit approval.** Drafting is not permission to run their tasks or alter product code. If no justified agent work exists, do not manufacture skills.
