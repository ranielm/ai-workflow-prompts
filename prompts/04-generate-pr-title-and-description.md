# Generate PR title + description and update PR_DESCRIPTION.md

Generate a Pull Request title and description based on the current branch changes compared to origin/develop.

Steps:
1. Run: git fetch origin develop
2. Run: git diff origin/develop --stat
3. Run: git diff origin/develop --name-only
4. Run: git log origin/develop..HEAD --oneline
5. Extract ticket ID from branch name (VAN-XXXX)
6. Analyze changes to understand scope and intent

PR title format (outside the description block):
type(VAN-XXXX): imperative short description

Type mapping:
- bugfix branch -> fix
- feature branch -> feat
- chore branch -> chore
- improvement branch -> improvement

PR description template (must not exceed 3000 characters):

{Concise overview of the changes. Mention the purpose and the problem it solves.}

---

## Ticket Link
* [JIRA Ticket: VAN-XXXX](REPLACE_WITH_YOUR_TICKET_URL)

---

## Tasks Completed
* [x] Task 1
* [x] Task 2
* [x] Task 3

---

## How to Test
- [ ] Step 1
- [ ] Step 2
- [ ] Step 3

---

## Additional Notes
{Impacted areas, limitations, dependencies}

Output:
1) Print PR title (single line)
2) Print PR description (template)
3) Create or update PR_DESCRIPTION.md in the repo root with ONLY the description body (no title line)
