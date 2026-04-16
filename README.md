# Global Codex Setup

This repository uses the live `~/.codex` directory as the local git working tree.

## Tracked files

- `AGENTS.md`
- `config.toml`
- `skills/product-tactician/SKILL.md`
- `skills/architect/SKILL.md`
- `skills/coder/SKILL.md`
- `skills/code-simplifier/SKILL.md`
- `skills/build-validator/SKILL.md`
- `skills/tester/SKILL.md`
- `skills/pr-helper/SKILL.md`

## Intentionally not tracked

Machine state, secrets, and generated files stay out of git, including:

- `auth.json`
- logs and sqlite files
- sessions
- caches
- plugins cache
- shell snapshots
- memories
- system skills

## Notes

- This repo is for durable global Codex behavior only.
- Repo-specific commands, folder layouts, and team conventions should stay in each repo's local `AGENTS.md`.
- `config.toml` may contain machine-specific project trust entries, so review changes before pushing them.
