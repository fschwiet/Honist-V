# Honist-V

A Claude Code plugin.

## Layout

The plugin lives under [`plugin/`](plugin/) so that a Claude Code session started in this repository does **not** auto-discover its skills, commands, or agents (that would require them to sit under `.claude/`). Keeping them in `plugin/` lets you develop the plugin here without it activating on itself.

```
plugin/
├── .claude-plugin/
│   └── plugin.json        # plugin manifest
├── commands/              # slash commands
├── skills/                # skills (each in its own folder with SKILL.md)
└── agents/                # subagents
```

## Verification

The verification pipeline is linting only:

```bash
pnpm install
pnpm verify          # runs format:check + lint
```

Other useful scripts:

| Script              | Description                      |
| ------------------- | -------------------------------- |
| `pnpm lint`         | Run ESLint                       |
| `pnpm format`       | Format all files with Prettier   |
| `pnpm format:check` | Check formatting without writing |

CI runs `pnpm verify` on every push and pull request (see [`.github/workflows/ci.yml`](.github/workflows/ci.yml)).
