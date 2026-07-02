# grill-with-docs

Documentation-aware design interviewer that challenges a plan against the project's existing language and decisions, updating CONTEXT.md and ADRs as terms and trade-offs are resolved.

## Usage

Triggers when the user wants to stress-test a plan against their project's domain model, glossary, or documented decisions.

## What it does

- Interviews the user about every aspect of a plan or design, one question at a time
- Resolves decision branches in dependency order with a recommended answer for each
- Explores the codebase instead of asking when a question can be answered that way
- Reads `CONTEXT.md` (or contexts via `CONTEXT-MAP.md`) and challenges fuzzy or conflicting terminology against the existing glossary
- Updates `CONTEXT.md` inline as terms are sharpened — glossary only, no implementation details
- Offers ADRs sparingly — only when the decision is hard to reverse, surprising without context, and the result of a real trade-off
- Creates `CONTEXT.md` and `docs/adr/` lazily, only when there's something to write

## Bundled references

- [CONTEXT-FORMAT.md](./references/CONTEXT-FORMAT.md) — glossary file shape and single vs multi-context layout
- [ADR-FORMAT.md](./references/ADR-FORMAT.md) — decision record shape and the criteria for when one is warranted
