# GitHub Contribute Template

This repository is a **template for AI coding assistants** (Claude Code, Cursor, OpenCode, etc.)
to set up GitHub community files and contributing guidelines in any repository — new or existing.

## Step 1: Detect Repository State

Before doing anything, check the target repository:

1. **Check if code already exists** — look for source files, `package.json`, `go.mod`, `pyproject.toml`,
   `Cargo.toml`, `Makefile`, `Dockerfile`, `docker-compose.yml`, etc.
2. **Check if community files already exist** — look for `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`,
   `.github/` directory, `LICENSE`, etc.
3. **Check for existing CI** — look for `.github/workflows/`, `.gitlab-ci.yml`, `Jenkinsfile`, etc.

### If existing repository with code:

- **Explore the codebase first** to understand:
  - Languages and frameworks used (read config files, source directories)
  - Package manager (`package.json` → npm/yarn/pnpm, `pyproject.toml` → uv/pip, `go.mod` → Go modules, etc.)
  - Existing linters/formatters (ESLint, Prettier, ruff, golangci-lint, etc.)
  - Test framework and test locations (look for test files, test config, test scripts)
  - Build commands (check `scripts` in package.json, `Makefile` targets, etc.)
  - Project structure (monorepo? multiple apps? library?)
  - Existing CI workflows (if any — preserve and extend, don't overwrite)
  - Database or service dependencies (Docker Compose, env vars, etc.)
- **Use discovered information** to fill templates automatically — don't ask user for info you can derive from code
- **Preserve existing files** — if `CONTRIBUTING.md` or other community files already exist,
  ask user whether to replace or merge

### If new/empty repository:

- Ask user for all required information (see Step 2)
- Generate everything from templates

## Step 2: Ask the User

**Always ask** (cannot be derived from code):
- Contact email (for Code of Conduct and Security reporting)
- License preference (MIT, Apache 2.0, GPL, etc.) or none

**Ask only if not detectable from existing code:**
- Project name
- Project description (one line)
- GitHub repository URL (e.g., `https://github.com/org/repo`)
- Tech stack / languages used
- Default branch name (check `git` first — `git branch --show-current` or `git remote show origin`)

## Step 3: Generate Files

Use template files from this repository as the base. For each file:

1. Replace all `[TODO: ...]` placeholders with actual values (user-provided or discovered from code)
2. Adapt content to match the project's actual tech stack
3. Remove sections that don't apply

### For existing repos — generate from real project data:

**CONTRIBUTING.md:**
- Prerequisites: list actual tools found in the project (read from config files)
- Development setup: write real steps based on how the project actually runs
- Code style: document actual linters/formatters found in config
- Testing: document actual test framework, test location, and commands
- Commit scopes: derive from project's directory structure / modules

**CI Workflow (`.github/workflows/ci.yml`):**
- If CI already exists: ask user whether to keep, replace, or extend
- If no CI: generate workflow based on actual project tooling:
  - Detect runtime version from `.node-version`, `.python-version`, `go.mod`, `rust-toolchain.toml`, etc.
  - Use actual lint/test/build commands from package manager scripts or Makefile
  - Add service containers if project uses Docker Compose for databases
  - Set correct trigger branches

**Security Policy (`.github/SECURITY.md`):**
- Architecture table: scan for auth, middleware, crypto, validation directories
- Sensitive areas: list actual security-critical paths found in the codebase

**PR Template:**
- Testing checklist: use actual test/lint/build commands from the project
- Remove screenshot/UI sections if project has no frontend

**Issue Templates:**
- Environment fields: match actual runtime/tools used by the project

## Template Files Reference

| File | Purpose |
|------|---------|
| `CODE_OF_CONDUCT.md` | Contributor Covenant v2.1 — replace email placeholder |
| `CONTRIBUTING.md` | Full contributing guide — customize for tech stack |
| `.github/SECURITY.md` | Security policy — replace email, repo URL, architecture |
| `.github/pull_request_template.md` | PR template — adapt checklists to tech stack |
| `.github/ISSUE_TEMPLATE/bug_report.md` | Bug report — replace project name, environment fields |
| `.github/ISSUE_TEMPLATE/feature_request.md` | Feature request — replace project name |
| `.github/ISSUE_TEMPLATE/config.yml` | Issue config — replace docs URL |
| `.github/workflows/ci.yml` | CI placeholder — build entirely based on tech stack |
| `LICENSE` | Placeholder — generate based on user's license choice |

## Customization Details

### CONTRIBUTING.md
- Prerequisites section: list actual tools needed (runtime, package manager, database, etc.)
- Development setup: write real steps for cloning, installing, running
- Commit scopes: define scopes relevant to the project's modules
- Code style: document actual linters, formatters, and conventions
- Testing: document actual test frameworks and commands

### CI Workflow
- The `ci.yml` is a minimal placeholder with comments
- Build real workflow steps based on the project's actual tech stack
- Common patterns: lint, typecheck, test, build
- Add service containers if needed (database, Redis, etc.)

### Security Policy
- Architecture table: document actual auth, authorization, and security mechanisms
- Sensitive areas: list actual directories/files that need extra review

### PR Template
- Testing checklist: match actual test/lint/build commands
- Add project-specific checklist items as needed
