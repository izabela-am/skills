# skills

Personal Claude Code skills.

| Skill | What it does |
|-------|--------------|
| [`study-tutor`](study-tutor/) | Socratic study tutor — dependency-graph placement, transfer-based explain-back gate, decay-aware recalibration, self-maintained per-subject state on disk. |
| [`grill-me`](grill-me/) | Interviews you relentlessly about a plan or design until reaching shared understanding, resolving each branch of the decision tree. |
| [`grill-with-docs`](grill-with-docs/) | Grilling session that challenges your plan against the existing domain model, sharpens terminology, and updates docs (CONTEXT.md, ADRs) inline as decisions crystallise. |
| [`handoff`](handoff/) | Compacts the current conversation into a handoff document for another agent to pick up. |
| [`skill-smith`](skill-smith/) | Meta-skill that creates, refines, and reviews the other skills here — grill-style design interview, failure-mode diagnosis, quality checklist. |
| [`capture`](capture/) | Appends a thought verbatim to today's daily note in the Obsidian vault — frictionless burst capture from any terminal. |
| [`learned`](learned/) | Distills the generalizable concepts from a work session into atomic zettels in the Obsidian vault, applying the vault contract's "public blog post" test. |
| [`writing`](writing/) | Applies Strunk's *Elements of Style* rules and avoids common AI writing patterns when writing prose for humans — docs, commit messages, UI text. |

## Using a skill

Make it discoverable by symlinking (or copying) the skills directory into a skills path — e.g. globally:

```sh
ln -s ~/dev/skills ~/.agents/skills
```
