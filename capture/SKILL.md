---
name: capture
description: Append a thought to today's daily note in the Obsidian vault at ~/dev/vault. Use when the user wants to capture, jot down, or note something for today — "capture this", "add to my daily note", "jot this down" — from any project or context.
---

Append the user's thought to today's daily note in the vault at `~/dev/vault`.

**First, read `~/dev/vault/CLAUDE.md`.** It is the contract for the vault and overrides anything in this skill. This skill only adds the workflow below; all rules about structure, naming, linking, and what may enter the vault live in the contract.

## Workflow

1. If the user gave no text to capture, ask what they want to capture. Otherwise use their words.
2. Get today's date: `date +%Y-%m-%d` for the filename, `date "+%A, %B %-d, %Y"` for the heading.
3. Target file is `~/dev/vault/Daily/<YYYY-MM-DD>.md`. If it doesn't exist, create it from the daily template shape defined in the contract (a single `# <Weekday, Month D, YYYY>` heading, nothing else).
4. Append the capture to the bottom of the file, **verbatim**. This is burst capture: keep the user's wording as written — do not rewrite, summarize, title, or restructure it. Fixing an obvious typo is fine only if the user asks.
5. If the capture references a note that clearly already exists in the vault by name, you may turn that mention into a `[[wikilink]]` — nothing more.
6. Run `~/dev/vault/.sync/vault-sync.sh` for an immediate commit-and-push (the contract permits this after a writing task).
7. Confirm with one line: what was appended and to which file. No follow-up suggestions, no offers to organize — the vault is designed to survive neglect.

## Boundaries

- Only ever append to **today's** note. Past daily notes are a frozen record.
- One capture per invocation; if the user rattles off several distinct thoughts, append them as separate lines but still verbatim.
- Never add frontmatter, tags, or extra sections.
