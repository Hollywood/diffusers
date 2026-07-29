# Skill: Implement Code from Plan

**Trigger:** Use when a user asks to build, scaffold, or implement an approved plan.

## Execution Steps:
1. **Identify Persona:** Note the user's stated role in the prompt (e.g., PM, Dev, QA, DevOps). Tailor the depth, focus, and technical terminology of your response to fit this persona.
2. **Context Gathering:** Locate and read the approved plan (either from chat history or a saved `.md` file). Restate the scope.
3. **Implementation:** 
   - Write the necessary Python classes/functions to scaffold a correct first contribution[cite: 1].
   - Ensure you follow the repository patterns identified in the plan.
4. **Strict Boundaries:** Do not perform unrelated cleanup. Do not invent new features outside the approved scope.
5. **Handoff:** Once the code is written, instruct the user to run the `@validate-quality` skill.