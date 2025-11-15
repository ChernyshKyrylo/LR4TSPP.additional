# Event App
Mobile application for organizing events.

## Features
- Create events
- Manage participants

## Setup Instructions
- Open the project in VS Code
- Use the Source Control view to initialize Git and manage commits, branches, and syncing

## Project Structure
```
event-app/
├─ src/
│  └─ index.html
├─ docs/
│  └─ readme.md
└─ commits.txt
```

## Git Workflow in VS Code for this project
- Initialize repository via Source Control
- Create branches via the status bar (Create Branch)
- Stage changes with the "+" button, commit with the checkmark, push via the "..." menu
- Use Fetch before Pull to mark asynchronous remote updates

Commit messages used:
- "Add initial HTML file"
- "Add blue CSS style to heading"
- "Add initial documentation"
- "Change heading text"
- "Add setup documentation"
- "Resolve merge conflict"
- "Revert added paragraph"
- "Asynchronous fetch for remote changes"

## Alternative path
- Alternative path: revert to restore previous state
- Use Revert Commit in VS Code to create a new commit that undoes specific changes while preserving history

## Undo vs Discard in VS Code
- Undo Last Commit - removes the last commit while keeping your changes available for re-commit
  - Console analog: `git reset --soft HEAD~1`
- Discard Changes - discards modifications in files and reverts them to the last committed state
  - Console analog: `git restore --staged --worktree <path>` or legacy `git checkout -- <path>`

## Cherry-pick explanation
- `git cherry-pick <commit>` applies the changes introduced by the specified commit onto the current branch
- Use case: bring a specific fix from another branch without merging the entire branch
- Steps used in this project:
  1. Copy the SHA of the desired commit from the Source Control history
  2. Run `git cherry-pick <sha>` in the built-in terminal
  3. Resolve conflicts in VS Code if needed, stage, and complete the cherry-pick commit