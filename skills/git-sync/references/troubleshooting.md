# Git Troubleshooting Guide

## Handling Rebase Conflicts

If `git pull --rebase` results in a conflict:
1. **Locate**: Use `git status` to find unmerged paths.
2. **Resolve**: Open the files, address the `<<<<<<<`, `=======`, `>>>>>>>` markers.
3. **Continue**:
   ```bash
   git add <resolved-files>
   git rebase --continue
   ```

## Handling Push Denials

If `git push` is rejected:
1. Ensure a `pull` was performed.
2. Check if another device has pushed newer commits.
3. Re-execute the Remote Alignment step.
