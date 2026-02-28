---
name: git-sync
description: Synchronizes the local project with GitHub. Use for routine backups, multi-device handoffs, or session closures. It automates the pull-rebase-commit-push sequence to ensure project integrity across different environments.
---

# Git Sync Skill

Provides a reliable way to mirror the "Small Universe" between physical local storage and the remote git vessel.

## Procedures

### 1. Verification
Check the current state of the workspace using `git status`. Identify if there are uncommitted materials or incoming gravity from the remote.

### 2. Remote Alignment
Perform `git pull --rebase`. 
- **Conflict?** → Refer to [references/troubleshooting.md](references/troubleshooting.md) immediately.

### 3. Local Consolidation
If changes exist:
1. Stage all: `git add .`
2. Commit with meaningful context or a standard chore message: `chore: sync [YYYY-MM-DD HH:MM]`.

### 4. Propulsion (Push)
Execute `git push`. Confirm total synchronization status.

## Decision Guidelines

- **Diverged History**: If local and remote have diverged, the Agent must attempt a rebase before pushing.
- **Merge Conflicts**: This is a "Low Freedom" scenario—stop and consult the troubleshooting guide or the User.

## Finished Pattern

After completion, the Agent should emit a **🛰️ Sync Report** summarizing Pull results, file counts, and Push success.
