# Agent Guidance

## Read first

Read `CLAUDE.md` for project context and its `## Active Handoff` for current
state. The shared private Codex guidance in `~/.codex/AGENTS.md` supplies
cross-project safety rules. Before changing files, inspect `git status` and
recent history.

## Project workflow

- This is an unmaintained Home Assistant HACS integration; preserve upstream
  compatibility and avoid unrelated changes.
- Component code is under `custom_components/southern_company/`.
- Never place Home Assistant or utility credentials in the repository.
- Run `pre-commit run --all-files` and the available focused Python checks
  before proposing a commit. A Home Assistant deployment or reload is live
  infrastructure and requires explicit direction.

## Handoff

Until the handoff is extracted to `handoff/ACTIVE.md`, update the existing
`## Active Handoff` section in `CLAUDE.md` after meaningful work. Keep entries
concise: current state, validation, open work, and risks.
