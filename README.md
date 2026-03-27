# Agent Skills

A curated collection of Claude Code skills for daily development workflows — installable as a marketplace plugin.

## Installation

```bash
claude marketplace add SiyuQian/agent-skills
```

This registers the plugin as `siyu@agentskill-marketplace`. After installation, the skills are available in all your Claude Code sessions.

## Available Skills

### pr-or-mr

Create and update pull requests (GitHub) or merge requests (GitLab) with well-structured descriptions.

- Auto-detects platform (GitHub / GitLab)
- Reads the actual diff before writing — no guessing from branch names
- Uses existing project PR/MR templates when available
- Falls back to built-in templates (frontend/backend × feature/bugfix)
- Generates a Review Guide section for reviewers
- Handles PR updates and draft → ready transitions

**Triggers on:** "create pr", "open pull request", "submit mr", "push for review", "update the pr", "mark as ready", "/pr", "ship it", and more.

## Awesome Skills & Plugins

Other great Claude Code skills and plugins worth checking out:

| Category | Plugin | Description |
|----------|--------|-------------|
| Frontend & Design | [impeccable](https://github.com/pbakaus/impeccable) | Expert frontend design skill with 17 commands for auditing, polishing, and steering UI quality |
| Workflow & Process | [superpowers](https://github.com/obra/superpowers) | Brainstorming, TDD, debugging, planning workflows |
| Spec & Planning | [OpenSpec](https://github.com/Fission-AI/OpenSpec) | Spec-driven development |

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to add skills or improve existing ones.

## License

[MIT](LICENSE)
