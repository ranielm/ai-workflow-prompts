# AI Workflow Prompts

A collection of prompts and templates to boost developer productivity using AI tools like Claude Code.

This repository accompanies the Medium article: **"How I Use AI (Claude Code) to Ship Faster as a Senior Frontend Engineer"**

## What's Inside

### Prompts

| File | Purpose |
|------|---------|
| [01-bug-report-creator.md](prompts/01-bug-report-creator.md) | Turn rough bug descriptions into formatted Jira tickets with branch commands and Claude Code prompts |
| [02-jira-task-processor.md](prompts/02-jira-task-processor.md) | Process existing Jira tickets and generate implementation prompts |
| [03-document-in-claude-md.md](prompts/03-document-in-claude-md.md) | Auto-document changes in CLAUDE.md files for future reference |
| [04-generate-pr-title-and-description.md](prompts/04-generate-pr-title-and-description.md) | Generate PR titles and descriptions from git diffs |

### Examples

| File | Purpose |
|------|---------|
| [pr-description-example.md](examples/pr-description-example.md) | Sample PR description output |

## How to Use

1. **Copy the prompt** you need from the `prompts/` folder
2. **Customize placeholders** (like `VAN-XXXX` project key) to match your setup
3. **Paste into Claude** (Web, Desktop, or Code) and provide your input
4. **Iterate** - adjust the prompts to fit your team's conventions

## Workflow Overview

```
Idea/Bug -> [01] Bug Report Creator -> Jira Ticket
                                            |
                                            v
Jira Ticket -> [02] Task Processor -> Branch + Implementation Prompt
                                            |
                                            v
Implementation -> [03] Document in CLAUDE.md -> Commit
                                            |
                                            v
Ready for PR -> [04] PR Generator -> PR Title + Description
```

## Customization Tips

- Replace `VAN` with your Jira project key
- Adjust branch naming conventions (`bugfix/`, `feature/`, etc.)
- Modify the PR description template to match your team's format
- Add your own ticket URL base path

## Disclaimer

- These prompts are templates - customize them for your specific needs
- Always review AI-generated content before committing
- Keep sensitive/proprietary information out of public prompts
- Examples are sanitized - replace placeholders with your actual data

## Contributing

Feel free to open issues or PRs with improvements!

## License

MIT
