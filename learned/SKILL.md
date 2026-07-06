---
name: learned
description: Distill the generalizable concepts from the current work session into atomic zettels in the Obsidian vault at ~/dev/vault. Use at the end of a meaty session, or when the user says "/learned", "save what we learned", "that's worth a zettel", or wants a session insight in their second brain.
allowed-tools: Read(~/dev/vault/**), Grep, Glob, Write(~/dev/vault/**), Edit(~/dev/vault/**), Bash(~/dev/vault/.sync/vault-sync.sh)
---

Harvest what this session taught and write it into the vault at `~/dev/vault` as one or more atomic zettels.

**First, read `~/dev/vault/CLAUDE.md`.** It is the contract for the vault and overrides anything in this skill. This skill only adds the workflow below; all rules about structure, naming, linking, templates, and what may enter the vault live in the contract.

## Workflow

### 1. Mine the session

Review the current conversation for insights that are **concepts, not work specifics** — learned patterns, techniques, gotchas, and mental models that would still be true and useful a year from now, on a different project. Debugging sessions are rich ore: the durable insight is rarely "we fixed X" but "systems of kind Y fail in way Z because W".

Apply the contract's test before anything else: generalize each candidate to what would survive **unredacted in a public blog post**. Strip customer data, credentials, internal hostnames, company or partner names, and unpatched-vulnerability details. If an insight cannot be generalized past its specifics, it does not become a zettel.

If the user pointed at a specific insight, focus there; otherwise select candidates yourself.

### 2. Propose, then wait

Present 1–3 candidates, each as:

- a **claim-shaped title** — a plain descriptive assertion that could stand alone as a filename (this is the hard part; the title carries the insight and makes search work)
- a two-or-three-sentence body draft

Fewer, better candidates beat coverage. If the session taught nothing durable, say so and stop — an empty harvest is a valid result.

Wait for the user to pick, edit, or reject before writing anything.

### 3. Write the chosen zettels

For each approved candidate:

1. Search the vault (filenames first, then full text) for related notes to link to — a zettel is finished when it points somewhere.
2. Write it to `Notes/` (flat), filename exactly equal to the title, matching the zettel template shape from the contract exactly: title heading, body, `## Links` section with `[[wikilinks]]`. No frontmatter, no tags, no extra sections.
3. If genuinely no existing note fits as a link, end with a one-line note-to-self explaining why, per the contract.
4. Keep the body atomic — one claim per zettel. If a candidate contains two ideas, it is two zettels.

### 4. Finish

Run `~/dev/vault/.sync/vault-sync.sh` for an immediate commit-and-push, then confirm what was written with `[[titles]]`. Do not propose cleanups, MOCs, or reviews — the vault's anti-rot triggers handle that during use.
