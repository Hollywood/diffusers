# Skill: Validate Quality and CI Guardrails

**Trigger:** Use when QA, DevOps, or a Developer asks to test, audit, or review a change.

## Execution Steps:
1. **Identify Persona:** Note the user's stated role in the prompt (e.g., PM, Dev, QA, DevOps). Tailor the depth, focus, and technical terminology of your response to fit this persona.
2. **Explore Guardrails:**
   - Read `.cursor/rules/200-testing-and-quality.mdc`.
   - Read `.cursor/rules/300-review-and-guardrails.mdc`.
3. **Test Generation:** If tests are missing, generate mock tests avoiding external downloads to catch mistakes early[cite: 1].
4. **Validation:** 
   - Provide the exact `pytest` command to run on the affected files.
   - Remind the user to run `ruff check .` to verify formatting and CI boundaries[cite: 1].
5. **Audit:** Separate findings into blocking vs. non-blocking based on the CI boundaries.
6. **Handoff:** If passing, instruct the user to run the `@generate-handoff` skill.