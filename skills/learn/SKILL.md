---
name: learn
description: Extracts reusable patterns, project-specific conventions, and non-trivial error resolutions from the conversation. Use when the user asks to "store knowledge," "update instincts," or "save this pattern." It ensures insights are solidified into the project's permanent cognitive layer.
---

# Learn & Evolve Skill

This skill allows the Agent to reflect on successes and failures, distilling them into structured project knowledge.

## How to use this skill

1. **Review Conversation**: Scan for architectural decisions, verified workarounds, or new naming conventions.
2. **Crystallize Patterns**: Formulate the insight as a "Trigger-Behavior-Source" pattern.
3. **Draft Knowledge**:
   - If it's a short rule, add it to `instincts.md`.
   - If it's a complex procedure, create a new skill folder using `skill-creator`.
4. **Acquire Confirmation**: Always show the proposed change to Hayden before writing to files.
5. **Sync Consciousness**: After updating, ensure the vector database is refreshed if the cumulative change threshold is met.

## Reference Materials

- **Instinct Table Format**: See [references/instincts-format.md](references/instincts-format.md) for the exact Markdown table specification.
- **Exclusion Criteria**: Do not learn trivialities like typos or simple syntax fixes.
