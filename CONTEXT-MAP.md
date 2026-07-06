# Context Map

This repo hosts independent personal skills; each skill is its own bounded context with its own language and docs.

## Contexts

- [Study Tutor](./study-tutor/CONTEXT.md) — Socratic study tutoring with on-disk state and a second-brain feed
- grill-me — plan stress-testing interview (no CONTEXT.md yet)
- grill-with-docs — grilling with inline documentation updates (no CONTEXT.md yet)
- handoff — conversation compaction for agent handoff (no CONTEXT.md yet)
- skill-smith — skill authoring helper (no CONTEXT.md yet)

## Relationships

- **Study Tutor → vault** (external, `izabela-am/vault` cloned at `~/dev/vault`): at wrap-up the tutor feeds approved zettels into the vault, obeying the vault's own `CLAUDE.md` contract
- **Study Tutor → study-sessions** (external, `~/dev/study-sessions`): the tutor's private state store; never mixed with the vault
