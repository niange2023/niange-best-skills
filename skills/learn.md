---
name: learn
description: Extract reusable patterns from the current session and save as skills.
---

# Learn Command

Analyze the current session and extract patterns worth saving as skills.

## When to Use

Run `/learn` at any point during a session when you've:
- Solved a non-trivial problem
- Discovered a useful pattern
- Found a workaround for a library quirk
- Learned project-specific conventions

## What to Extract

1. **Error Resolution Patterns**
   - What error occurred?
   - What was the root cause?
   - What fixed it?

2. **Debugging Techniques**
   - Non-obvious debugging steps
   - Tool combinations that worked

3. **Project-Specific Patterns**
   - Codebase conventions discovered
   - Architecture decisions made

4. **Workarounds**
   - Library quirks
   - API limitations

## Process

1. Review the session for extractable patterns
2. Identify the most valuable/reusable insight
3. Draft a skill file
4. Ask user to confirm before saving
5. Save to `skills/<skill-name>/SKILL.md` or update `instincts.md`

## Don't Extract

- Trivial fixes (typos, simple syntax errors)
- One-time issues (specific API outages)
- Obvious patterns that are well-documented

## Related Skills

This command works with:
- `skills/ContinuousLearning/SKILL.md` - Instinct-based learning system
