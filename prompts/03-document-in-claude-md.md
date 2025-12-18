# Document current work in CLAUDE.md

Document the current work in a CLAUDE.md file.

Steps to execute:

1) Get current branch name:
- Run: git branch --show-current
- Extract ticket ID from branch name (VAN-XXXX)

2) Get changes summary:
- Run: git diff origin/develop --stat
- Run: git diff origin/develop --name-only
- Run: git log origin/develop..HEAD --oneline

3) Identify the most appropriate folder:
- Analyze the changed files
- Find the common parent folder or main feature folder
- If changes span multiple areas, use the project root

4) Create or append to CLAUDE.md in that folder with this format:

{ticket-id}: {brief-description-from-branch}
Date: {current-date}
Changes:
{file-1}: {what-was-done}
{file-2}: {what-was-done}
{file-3}: {what-was-done}

Summary:
{one-paragraph-summary}

5) Stage the CLAUDE.md file:
- Run: git add {path-to-CLAUDE.md}

6) Commit:
- Run: git commit -m "docs({scope}): document {ticket-id} implementation"

7) Push:
- Run: git push origin {current-branch}

Output (only):
- Documented in {path-to-CLAUDE.md}
- Committed: docs({scope}): document {ticket-id} implementation
- Pushed to origin/{branch-name}

Be brief. No extra commentary.
