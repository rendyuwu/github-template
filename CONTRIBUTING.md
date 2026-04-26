# Contributing to [TODO: PROJECT_NAME]

Thank you for your interest in contributing to [TODO: PROJECT_NAME]. This guide covers everything you need to get started.

## Prerequisites

<!-- [TODO: List actual tools, runtimes, and system dependencies needed] -->

- Git
- [TODO: Runtime] (e.g., Node.js 20+, Python 3.12+, Go 1.22+, etc.)
- [TODO: Package manager] (e.g., npm, uv, cargo, etc.)
- [TODO: Other tools] (e.g., Docker, database, etc.)

## Development Setup

### 1. Fork and clone

```bash
git clone https://github.com/<your-username>/[TODO: REPO_NAME].git
cd [TODO: REPO_NAME]
```

### 2. Install dependencies

<!-- [TODO: Write actual install commands for your project] -->

```bash
# Example:
# npm install
# uv sync
# go mod download
```

### 3. Configure environment

<!-- [TODO: Describe environment setup if needed (.env files, config, etc.)] -->

```bash
# cp .env.example .env
# Edit .env with your local settings
```

### 4. Run the project

<!-- [TODO: Write actual run commands] -->

```bash
# Example:
# npm run dev
# uv run uvicorn app.main:app --reload
# go run ./cmd/server
```

## Branch Naming

Use type-prefixed branches:

| Prefix | Purpose |
|--------|---------|
| `feat/` | New feature |
| `fix/` | Bug fix |
| `docs/` | Documentation only |
| `refactor/` | Code refactoring (no behavior change) |
| `test/` | Adding or updating tests |
| `chore/` | Build, CI, tooling changes |

Examples: `feat/user-auth`, `fix/login-redirect`, `docs/api-endpoints`

## Commit Messages

We use [Conventional Commits](https://www.conventionalcommits.org/).

```
<type>(<scope>): <subject>
```

### Types

`feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`, `perf`, `ci`, `revert`

### Scopes

<!-- [TODO: Define scopes relevant to your project's modules] -->

Examples: `api`, `ui`, `auth`, `db`, `config`, `ci`

### Rules

- Imperative mood: "add feature" not "added feature"
- Lowercase first letter
- No period at end
- Subject line max 50 characters

### Examples

```
feat(auth): add OAuth2 login flow
fix(api): handle null response from external service
docs(readme): update installation instructions
refactor(db): extract query builder into separate module
test(auth): add token expiry edge case tests
chore(ci): add lint step to CI workflow
```

## Pull Request Process

1. Create a feature branch from `[TODO: DEFAULT_BRANCH]`
2. Make your changes
3. Ensure all checks pass locally:

<!-- [TODO: Write actual check commands for your project] -->

```bash
# Lint
# npm run lint / ruff check / golangci-lint run

# Test
# npm run test / pytest -q / go test ./...

# Build (if applicable)
# npm run build / go build ./...
```

4. Push your branch and open a PR
5. Fill out the PR template completely
6. At least one approving review is required
7. Squash and merge after approval
8. Delete the branch after merge

## Code Style

<!-- [TODO: Document your project's code style conventions] -->

### Linting

- Linter: [TODO: linter name and config location]
- Run: `[TODO: lint command]`

### Formatting

- Formatter: [TODO: formatter name] (if separate from linter)
- Run: `[TODO: format command]`

### Conventions

<!-- [TODO: List key conventions — type hints, async patterns, import style, etc.] -->

- [TODO: Convention 1]
- [TODO: Convention 2]

## Testing

- Framework: [TODO: test framework]
- Location: [TODO: where tests live]
- Run: `[TODO: test command]`
- New features need happy-path + edge-case tests
- Bug fixes need regression tests

## Issue Guidelines

### Bug Reports

Use the [bug report template](.github/ISSUE_TEMPLATE/bug_report.md). Include:
- Steps to reproduce
- Expected vs actual behavior
- Environment details

### Feature Requests

Use the [feature request template](.github/ISSUE_TEMPLATE/feature_request.md). Include:
- Problem statement
- Proposed solution

### Labels

| Label | Purpose |
|-------|---------|
| `bug` | Something isn't working |
| `feature` | New feature request |
| `docs` | Documentation improvement |
| `good first issue` | Good for newcomers |
| `help wanted` | Extra attention needed |
| `duplicate` | Duplicate issue |
| `wontfix` | Will not be addressed |
| `security` | Security-related |

## Security

Do not open public issues for security vulnerabilities. See [SECURITY.md](.github/SECURITY.md) for reporting instructions.

Key security rules:
- Never commit secrets or credentials
- Auth-related changes require extra review
- Input sanitization must not be weakened
- Use parameterized queries for database access
