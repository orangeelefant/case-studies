# CLAUDE.md

Project context for Claude Code sessions in this repository.

## What This Is

Webraketen case study — Rastahunden (Sveriges hundvänliga karta)

**Live:** https://rastahunden.com

## Stack

_(Fill in: framework, language, hosting, key services. Inspect `package.json` / `pyproject.toml` / similar to confirm.)_

## Layout

- `src/` — source code
- `tests/` — tests
- `docs/` — documentation
- `scripts/` — utility scripts

## Commands

```bash
# install
# build
# test
# dev
```

_(Fill in actual commands once known.)`_

## Conventions

- Match existing patterns; don't introduce new abstractions without reason.
- Keep files under 500 lines.
- Swedish copy for client-facing text unless otherwise specified.
- Secrets live in `~/.secrets` and are referenced via `${VAR}`.

## Definition of Done

A change is done when:

1. Code works (built and verified locally).
2. `CHANGELOG.md` updated under `[Unreleased]`.
3. `TODO.md` reconciled (completed items removed or ticked, follow-ups added).
4. Committed and pushed to `main`.

See `AGENTS.md` for the full agent contract.
