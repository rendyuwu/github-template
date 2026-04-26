# Security Policy

## Supported Versions

| Version | Supported |
|---------|-----------|
| Latest `[TODO: DEFAULT_BRANCH]` | Yes |
| Older releases | [TODO: Define support policy] |

## Reporting a Vulnerability

**Do not open a public issue for security vulnerabilities.**

### How to Report

1. **Email:** Send details to **[TODO: CONTACT_EMAIL]**
2. **GitHub:** Use [GitHub's private security advisory](https://github.com/[TODO: GITHUB_ORG]/[TODO: REPO_NAME]/security/advisories/new)

### What to Include

- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if any)

### Response Timeline

| Stage | Timeline |
|-------|----------|
| Acknowledgment | Within 48 hours |
| Initial assessment | Within 5 business days |
| Fix (Critical) | 24-48 hours |
| Fix (High) | 1 week |
| Fix (Medium/Low) | Next release cycle |

### Disclosure Policy

We follow coordinated disclosure:

1. Reporter submits vulnerability privately
2. We acknowledge and assess
3. We develop and test a fix
4. We release the fix
5. We publicly disclose with credit to the reporter (unless anonymity requested)

## Security Architecture

<!-- [TODO: Document your project's security-relevant architecture] -->

| Area | Location | Notes |
|------|----------|-------|
| Authentication | [TODO: path] | [TODO: mechanism] |
| Authorization | [TODO: path] | [TODO: mechanism] |
| Input validation | [TODO: path] | [TODO: approach] |
| Secrets management | [TODO: path] | [TODO: approach] |

## Security-Sensitive Areas

Changes to these areas require extra review:

<!-- [TODO: List directories/files that handle security-critical logic] -->

- Authentication and session handling
- Authorization and permission checks
- Input validation and sanitization
- Secret/credential management
- Database migration scripts
- API route handlers that accept user input
