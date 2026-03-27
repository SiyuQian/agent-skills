# Default PR/MR Templates

Use when no project template exists. Pick the template that matches your change,
then **remove any section that doesn't apply** — don't leave empty headers.

PR title carries the type: use conventional commits (`feat:`, `fix:`, `refactor:`, `docs:`, `chore:`).

---

## Frontend Templates

### Frontend — Feature

```markdown
## Description

{What this feature adds and why, based on the actual diff}

## Review Guide

**Start here:** {The most important file/component to review first}

{Suggested review order, any tricky logic to watch for}

## Visual Changes

Before:

After:

## Verification

- [ ] `npm run lint` / `npx eslint .` passes
- [ ] `npm test` / test suite passes
- [ ] Tested in browser: {specific pages/flows to check}
- [ ] Responsive: tested at mobile, tablet, desktop widths
- [ ] Accessibility: keyboard navigation and screen reader tested

## For Reviewers (human)

- [ ] Self-review of the code
- [ ] Design matches spec/mockup
```

### Frontend — Bug Fix

```markdown
## Description

**Bug:** {What was broken — specific symptom, not "it didn't work"}

**Cause:** {Root cause found in the diff}

**Fix:** {What the code change does to resolve it}

## Review Guide

**Start here:** {The file with the core fix}

{Any related files that changed, why they needed to change too}

## Verification

- [ ] `npm run lint` / `npx eslint .` passes
- [ ] `npm test` / test suite passes
- [ ] Bug no longer reproduces: {exact steps to verify}
- [ ] No visual regressions in related pages

## For Reviewers (human)

- [ ] Self-review of the code
```

---

## Backend / Infra Templates

### Backend — Feature

```markdown
## Description

{What this feature adds and why, based on the actual diff}

## Review Guide

**Start here:** {The most important file/module to review first}

{Suggested review order, any tricky logic or architectural decisions to watch for}

## Verification

- [ ] `make test` / `go test ./...` / `pytest` passes
- [ ] `make lint` / linter passes
- [ ] API tested: {specific endpoints or commands to exercise}
- [ ] Migration tested (if applicable): {migration steps}

## Additional Notes

{Deploy dependencies, feature flags, environment variables, follow-up work — remove if nothing}

## For Reviewers (human)

- [ ] Self-review of the code
- [ ] Checked for security implications
```

### Backend — Bug Fix

```markdown
## Description

**Bug:** {What was broken — specific symptom}

**Cause:** {Root cause found in the diff}

**Fix:** {What the code change does to resolve it}

## Review Guide

**Start here:** {The file with the core fix}

## Verification

- [ ] `make test` / `go test ./...` / `pytest` passes
- [ ] `make lint` / linter passes
- [ ] Bug no longer reproduces: {exact steps to verify}
- [ ] No regressions in related functionality

## For Reviewers (human)

- [ ] Self-review of the code
```

---

## Template Selection

| Change Type | Frontend touches? | Template |
|---|---|---|
| New feature | Yes | Frontend — Feature |
| New feature | No | Backend — Feature |
| Bug fix | Yes | Frontend — Bug Fix |
| Bug fix | No | Backend — Bug Fix |
| Mixed (frontend + backend) | Both | Combine relevant sections from both |
| Docs / config only | Neither | Use just Description + Review Guide |

## Checklist Rules

**Verifiable items** (agent should run the command and fill in result):
- Lint, test, build commands — run them and report pass/fail
- If a command fails, leave unchecked and note the failure

**Human items** (leave for the reviewer):
- Always unchecked — the agent cannot perform these
- Clearly labeled under "For Reviewers (human)"

**Detecting project commands:**
- Check `package.json` scripts, `Makefile`, `pyproject.toml`, `.github/workflows/` for the actual lint/test/build commands
- Use the project's real commands, not generic placeholders
