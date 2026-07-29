# Skill: Plan Feature Contribution

**Trigger:** Use when a user asks to plan, scope, or spec a new feature or change.

## Execution Steps:
1. **Understand:** Read the user's prompt. Ask blocking questions to clarify the scope, API compatibility, and constraints. Do not write code.
2. **Explore:** 
   - Read `.cursor/rules/100-agent-workflows.mdc` for persona context.
   - Search the repository for existing patterns.
3. **Plan Output:** Generate a structured Markdown plan containing:
   - Business Impact
   - Proposed Approach & Affected Files
   - Testing Strategy
4. **Pause:** Stop and ask the user for approval. Once approved, instruct the user to run the `implement-code` skill.