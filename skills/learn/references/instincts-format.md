# Instinct Table Format

When updating `instincts.md`, all entries MUST conform to this Markdown table structure:

| ID | Trigger (When) | Behavior (What the Agent does) | Confidence | Domain | Source |
| :--- | :--- | :--- | :--- | :--- | :--- |

### Definitions
- **ID**: `sys-XXX` (System/Workflow), `tool-XXX` (Tools), or `lang-XXX` (Language).
- **Trigger**: The specific condition, command, or state that fires the instinct.
- **Behavior**: Clear, imperative description of the expected action.
- **Confidence**: 0.1 to 1.0 (How reliable this pattern is).
- **Domain**: The subsystem affected (e.g., architecture, content-gen, git).
- **Source**: Brief mention of the context (e.g., "Refactoring session", "Vector DB fix").
