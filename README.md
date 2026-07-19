# Honist-V

A Claude Code plugin,

- the parts of Jesse Vincent's Superpowers I use trimmed to how I use them (brainstorming, writing-plans, executing-plans, test-driven-development)
- a session start hook instruct Claude not to use the AskUserQuestion tool when it will clip its options

## Verification

The verification pipeline is linting only:

```bash
pnpm install
pnpm verify          # runs format:check + lint + lint:md
```

Other useful scripts:

| Script              | Description                      |
| ------------------- | -------------------------------- |
| `pnpm lint`         | Run ESLint                       |
| `pnpm lint:md`      | Lint Markdown with markdownlint  |
| `pnpm format`       | Format all files with Prettier   |
| `pnpm format:check` | Check formatting without writing |

CI runs `pnpm verify` on every push and pull request (see [`.github/workflows/ci.yml`](.github/workflows/ci.yml)).
