# Study Tutor

Socratic study tutoring optimized for durable understanding. The tutor keeps operational state in the study-sessions repo and feeds distilled knowledge into the user's second brain (the vault).

## Language

**Gate pass**:
A topic answer that clears the transfer step of the explain-back gate — applied to a novel instance, not just restated.
_Avoid_: done, completed, learned

**Zettel**:
An atomic, claim-titled, own-words note in the vault's `Notes/` folder. The unit of the second brain.
_Avoid_: note, summary, study note

**Zettel bar**:
The rule that only gate passes earn a zettel. Shaky and deferred topics wait until they pass.

**Second-brain feed**:
The wrap-up step where the tutor drafts zettels from the user's gate answers, gets approval, and writes them to the vault.
_Avoid_: sync, export, mirror

**Zettel debt**:
A gate-passed topic whose zettel hasn't been written yet (e.g. the vault was absent at wrap-up). Recorded as `zettel: pending` in `curriculum.md` and settled at the next wrap-up.

**State**:
The tutor's operational files in the study-sessions repo (curriculum, progress, flashcards, index). Never knowledge; never lives in the vault.

**Vault**:
The user's second brain — the Obsidian vault repo (`izabela-am/vault`, cloned at `~/dev/vault`), governed by its own `CLAUDE.md` contract.
_Avoid_: second-brain repo, notes repo
