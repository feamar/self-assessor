# Self Assessor

An evidence-first software delivery quality assessment skill for GitHub Copilot and other LLM agents.

The [Software Delivery Assessment skill](.github/skills/software-delivery-assessment/SKILL.md) examines a .NET codebase and test suites, reviews CI/CD history and quality reports (including BonCode and SonarQube), and interviews team members only where evidence is incomplete. It assesses delivery, testing, architecture, security, reliability, SRE practices and AI assurance with scoring under conventional, AI-assisted and AI-driven perspectives.

## Use in an IDE

1. Open the software repository to be assessed in GitHub Copilot agent mode (Visual Studio or VS Code with Agent Skills support).
2. Install this repository's `.github/skills/software-delivery-assessment/` folder in the target repository's corresponding `.github/skills/` folder, or use a supported personal skills location.
3. Ask: **"Assess this repository using the software-delivery-assessment skill. Collect read-only evidence first, then interview me about remaining gaps. Show all three assessment perspectives."**
4. Provide authorized CI/CD, incident and monitoring access or exports and BonCode/SonarQube reports where available.
5. Review the scored dimensions, evidence provenance, unknowns, confidence and unanswered questions.

The assistant must not treat lack of evidence as proof of poor performance, confuse reconstructed metrics with team-published metrics, or assume that source configuration proves historical execution. The skill is **an assessment guide**, not an executable service or preconfigured integration.

The source files are maintained under [`.github/skills/software-delivery-assessment/`](.github/skills/software-delivery-assessment/). See its [README](.github/skills/software-delivery-assessment/README.md) for prerequisites, caveats and the complete file index.

## Version

Initial import: v1.3 from the source ZIP prepared for the .NET pilot. Includes D26–D30 (incident learning, change size, rollout strategy, automation and SRE/monitoring) in addition to the earlier 25 dimensions.