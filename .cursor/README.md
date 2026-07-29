# Diffusers First PR Coach (Modular Context Engine)

## Business objective
Reduce the time required for a new engineer to produce a reviewable first contribution without increasing the burden on senior reviewers, while shaping one solution that serves multiple audiences (PM, QA, DevOps), not just an individual developer[cite: 1].

## Primary success measure
Time from receiving a scoped task to producing a review-ready pull request that safely fits the path to production and works with the team's CI and guardrails[cite: 1].

## Supporting measures
- Number of first-round review comments
- Number of failed CI attempts
- Number of convention-related findings caught before code review[cite: 1]
- Number of senior-engineer interruptions
- Expansion of tool utility to non-engineering roles (PMs, QA, and DevOps)[cite: 1]

## Architecture & Sources of truth
This solution uses an **Agentic Microservice** architecture combined with a **Pointer Pattern** to prevent LLM token bloat and ensure the solution stays maintainable as the library evolves[cite: 1]:
1. **Passive Routing:** `.cursor/rules/` (MDC files) act as background tripwires to catch mistakes early[cite: 1].
2. **Active Micro-Skills:** `.cursor/skills/` are decomposed into distinct SDLC phases so the agent only loads the context it needs.
3. **Deep Context:** Maintainer-owned `.ai/` documentation (triggered dynamically by MDC rules).
4. **Codebase:** Existing Diffusers source code and test suite.

## The Modular Workflow (Skill Chaining)
The monolithic process has been broken down into a guided command workflow for scoped tasks[cite: 1]. Users can chain these skills or trigger them independently based on their persona:

1. **`@plan-feature` (PM / Tech Lead):** Understands the scope, asks blocking architectural questions, and drafts the approach for human approval.
2. **`@implement-code` (Developer):** Scaffolds a correct first contribution following the library's conventions based on the approved plan[cite: 1].
3. **`@validate-quality` (QA / DevOps):** Strengthens tests, checks CI boundaries, and audits the diff against formatting and security guardrails before review[cite: 1].
4. **`@generate-handoff` (Cross-Functional):** Generates a multi-audience Change Brief featuring distinct views for Developers, QA, PMs, and DevOps[cite: 1].

## Deliberately excluded from version one
- Autonomous merging or deployment (human approval remains the gate)
- Custom model training or fine-tuning
- External MCP integrations or custom API wrappers (to minimize platform team maintenance)[cite: 1]
- A custom vector database