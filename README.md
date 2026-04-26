# GitHub Contribute Template

GitHub community files and contributing guidelines template, designed to be set up by AI coding assistants (Claude Code, Cursor, OpenCode, etc.).

Works for both **new repositories** and **existing projects** — the AI assistant will detect existing code and generate files based on the actual tech stack.

## What's Included

```
.
├── CLAUDE.md                              # Instructions for AI assistants
├── CODE_OF_CONDUCT.md                     # Contributor Covenant v2.1
├── CONTRIBUTING.md                        # Contributing guide (customizable)
├── LICENSE                                # License placeholder
├── README.md                              # This file
└── .github/
    ├── SECURITY.md                        # Security policy
    ├── pull_request_template.md           # PR template with checklists
    ├── ISSUE_TEMPLATE/
    │   ├── bug_report.md                  # Bug report template
    │   ├── feature_request.md             # Feature request template
    │   └── config.yml                     # Issue template config
    └── workflows/
        └── ci.yml                         # CI workflow placeholder
```

## Usage

### With an AI Coding Assistant

Give the assistant this repo URL and ask it to set up your project:

**New repository:**
```
Set up contributing guidelines and GitHub templates for my project
using this template: https://github.com/simondayce/github-contribute-template
```

**Existing repository:**
```
Set up contributing guidelines and GitHub templates for this repo
based on: https://github.com/simondayce/github-contribute-template
```

For existing repos, the AI assistant will explore your codebase first — detect languages, frameworks, linters, test tools, build commands — then generate files that match your actual project setup. It only asks for things it can't derive from code (email, license).

### Manual Setup

1. Copy all files (except `README.md` and `CLAUDE.md`) into your project
2. Search for `[TODO: ...]` placeholders and replace them with your project's values
3. Customize sections based on your tech stack
4. Delete sections that don't apply

## Template Placeholders

All templates use `[TODO: ...]` markers. Key placeholders:

| Placeholder | Description |
|-------------|-------------|
| `[TODO: PROJECT_NAME]` | Your project's display name |
| `[TODO: REPO_NAME]` | GitHub repository name |
| `[TODO: GITHUB_ORG]` | GitHub organization or username |
| `[TODO: CONTACT_EMAIL]` | Email for CoC and security reports |
| `[TODO: DEFAULT_BRANCH]` | Default branch (`main` or `master`) |

## Credits

Template structure inspired by [Project NOA](https://github.com/rendyuwu/noa).

## License

This template repository is public domain. Use it however you like.
The `CODE_OF_CONDUCT.md` is adapted from [Contributor Covenant v2.1](https://www.contributor-covenant.org/version/2/1/code_of_conduct.html).
