# Agent Skills

A Claude Code skills plugin repository. Each skill lives under `skills/<name>/SKILL.md`.

## Project Structure

```
skills/
├── google-go-style/   # Google Go Style Guide enforcement
│   ├── SKILL.md
│   ├── LICENSE.txt
│   └── references/    # 8 detailed style reference docs
├── learn/             # Single-article HTML digest generator
│   ├── SKILL.md
│   └── evals/
├── news-digest/       # Multi-source news briefing generator
│   ├── SKILL.md
│   └── evals/
└── pr-creator/        # PR/MR creation and update
    ├── SKILL.md
    ├── LICENSE.txt
    └── templates/     # Built-in PR/MR templates
```

## Plugin Config

- `.claude-plugin/plugin.json` — plugin metadata
- `.claude-plugin/marketplace.json` — marketplace registration

## Development

- Each skill is self-contained in its own directory
- `SKILL.md` is the entry point with frontmatter (name, description) and full instructions
- Some skills include `evals/` for testing and `references/` for supplementary docs
- See [CONTRIBUTING.md](CONTRIBUTING.md) for how to add or modify skills
