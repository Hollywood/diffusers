# Skill: Plan Feature Contribution

**Trigger:** Use when a user asks to plan, scope, or spec a new feature or change.

## Execution Steps:
1. **Identify Persona:** Note the user's stated role in the prompt (e.g., PM, Dev, QA, DevOps). Tailor the depth, focus, and technical terminology of your response to fit this persona.
2. **Understand:** Read the user's prompt. Ask blocking questions to clarify the scope, API compatibility, and constraints. Do not write code.
3. **Explore:** 
   - Read `.cursor/rules/100-agent-workflows.mdc` for workflow context.
   - Search the repository for existing patterns.
4. **Plan Output:** Generate a structured Markdown plan containing:
   - Business Impact
   - Proposed Approach & Affected Files
   - Testing Strategy
5. **Pause:** If the user is a Dev persona, stop and ask the user for approval. Once approved, instruct the user to run the `@implement-code` skill. If they are any other persona ask the user if they'd like a PDF version of the plan.