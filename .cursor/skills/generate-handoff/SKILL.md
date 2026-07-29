# Skill: Generate Multi-Role Handoff Brief

**Trigger:** Use when a change is complete and ready for review or deployment.

## Execution Steps:
1. **Identify Persona:** Note the user's stated role in the prompt (e.g., PM, Dev, QA, DevOps). Tailor the depth, focus, and technical terminology of your response to fit this persona.
2. **Analyze Diff:** Inspect `git diff --stat` and the full git diff for the current workspace.
3. **Generate Brief:** Produce a Change Brief with the following exact sections to serve the multiple audiences surrounding the engineering team[cite: 1]:
   - **Developer View:** Technical changes and follow-up work.
   - **QA View:** Edge cases and verified tests.
   - **PM View:** User problem solved and items deliberately excluded.
   - **DevOps View:** Dependency changes and deployment risks.