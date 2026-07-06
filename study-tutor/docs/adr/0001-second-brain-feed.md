# Feed the vault at wrap-up, gate-passes only, under the vault's own contract

The tutor feeds the user's second brain (`izabela-am/vault`, cloned at `~/dev/vault`) with atomic zettels, but only for topics that passed the transfer gate, only at wrap-up (one approval batch per session), and drafted strictly from the user's own explain-back phrasing. The skill does not carry the vault's format/naming/linking rules — it reads and obeys the vault's `CLAUDE.md` before writing, so there is exactly one contract and no drift.

## Considered Options

- **Mirror `progress.md` entries into the vault** — rejected: duplicates state and produces journal noise, not a linked knowledge network.
- **Zettels for shaky/deferred topics too** — rejected: the vault's value is that everything in `Notes/` is genuinely understood; the gate is the proof.
- **Live zettel per gate pass** — rejected: interrupts session momentum with per-topic approval stops; wrap-up batching gives one approval round and crashed sessions catch up via `zettel: pending` in `curriculum.md`.
- **Duplicating vault rules into SKILL.md** — rejected: two contracts drift; the vault's `CLAUDE.md` is authoritative.
- **Quizzing from zettels instead of `flashcards.md`** — rejected: flashcards are retrieval-practice state and must not couple the tutor to vault availability; duplication across the repo boundary is accepted.

## Consequences

- The vault is optional infrastructure: when `~/dev/vault` is absent, wrap-up records zettel debt and moves on — a study session never blocks on it.
- Changing the zettel bar later re-litigates the trust guarantee of every existing note in `Notes/`, so this bar should be treated as stable.
