# Three separate, concise leadership judgments

**Always produce three independent Markdown outcome files:** conventional, AI-assisted and AI-driven. Use sensible filenames and paths chosen for the service (e.g. `assessment-conventional.md`, `assessment-ai-assisted.md`, `assessment-ai-driven.md`). Identify perspective, assessed service/revision, period and a few decisive evidence references. **Each judgment: at most three paragraphs / one page** (aim 150–250 words), for lead developers and CTOs. No number or weighted score by default; if explicitly requested, use [internal calibration](perspectives.md).

**Paragraph 1 — Candid verdict and actual outcomes.** State clearly whether results are weak, good or truly excellent for this perspective and why. Discuss evidenced speed, reliability, recovery, cost/value and user outcomes. Do not sugarcoat poor results or pretend that unavailable measurements exist.

**Paragraph 2 — Evidence and confidence.** Tie praise or criticism to **actual CI/CD runs, code-quality reports (such as SonarQube), test outcomes, operational results and other source records** wherever available; inspect and corroborate them before judgment. Explain which sources were not available, the resulting confidence limits, code and test quality, mature SRE practice and critical safeguards. Excellent demands a sustained, credible trail, not a good-looking repository.

**Paragraph 3 — Improve or sustain.** For poor delivery, identify concrete high-impact corrections; for good delivery, acknowledge strengths and realistic gains; for excellent delivery, explicitly say **continue what demonstrably works**. No forced shortcomings. When AI-driven outcome measurements are missing, recommend **rigorous output measurement** as a priority, not an automatically drafted agent skill.

**Presentation:** The user's selected perspective (conventional by default) is the **only judgment displayed in the conversational summary**; provide access to the other two files and allow later selection **without rerunning**. Keep outcomes distinct, do not silently overwrite historical runs, and do not claim a file is saved or committed without confirmation.

**After reporting:** Once all three judgments are complete and the selected one is shown, offer one optional next step: **"Would you like me to draft instructions/skills for agents to address these findings?"** Do not create or attach agent skills until the developer explicitly opts in. This offer is outside the three-paragraph report, and must not distract from evidence or the verdict.

**Permission:** Generating three separate copy-ready Markdown judgments is the fallback where repository writing is not authorized. Creating or updating files in the assessed repository requires explicit permission. Supporting ledgers are separate on request; optional remediation skills require a later affirmative choice.
