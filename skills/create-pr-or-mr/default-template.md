# Default PR/MR Template

Use this when no project template exists. **Only include sections relevant to the change** —
remove sections entirely if they don't apply.

```markdown
## Description

{What this change does and why — from the actual diff, not assumptions}

Closes: #{issue_number}

## Type of Change

* [ ] Bug fix
* [ ] New feature
* [ ] Refactor
* [ ] Performance improvement
* [ ] Documentation update
* [ ] Breaking change

## How Has This Been Tested?

{Reference specific test files added/modified, or manual verification steps}

## Screenshots / Demo

{Only for visual changes — remove this section entirely for backend/library/infra/docs}

## Checklist

* [ ] I have performed a self-review of my code
* [ ] My code follows the project's coding standards
* [ ] I have added tests where necessary
* [ ] All tests pass locally
* [ ] Documentation has been updated if required
* [ ] This PR is ready for review

## Additional Notes

{Migration steps, deploy dependencies, follow-up work — remove if nothing to say}
```

## Section Rules

| Section | Include when | Remove when |
|---------|-------------|-------------|
| Description | Always | Never |
| Closes: line | Related issue exists | No linked issue |
| Type of Change | Always | Never |
| How Has This Been Tested? | Functional changes | Docs-only or config changes |
| Screenshots / Demo | UI, visual, or CLI output changes | Backend, library, infra, docs |
| Checklist | Always | Never |
| Additional Notes | Migration, deploy notes, or context | Nothing extra |

## Checklist Honesty

Only check (`[x]`) items you have actually verified:
- Did you run the tests? Then check "All tests pass locally"
- Did you not run the tests? Leave it unchecked
- Pre-checking everything is dishonest and defeats the purpose
