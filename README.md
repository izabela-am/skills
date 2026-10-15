# skills

Personal Claude Code skills.

| Skill | What it does |
|-------|--------------|
| [`grill-me`](grill-me/) | Interviews you relentlessly about a plan or design until reaching shared understanding, resolving each branch of the decision tree. |
| [`grill-with-docs`](grill-with-docs/) | Grilling session that challenges your plan against the existing domain model, sharpens terminology, and updates docs (CONTEXT.md, ADRs) inline as decisions crystallise. |
| [`handoff`](handoff/) | Compacts the current conversation into a handoff document for another agent to pick up. |
| [`writing`](writing/) | Applies Strunk's *Elements of Style* rules and avoids common AI writing patterns when writing prose for humans — docs, commit messages, UI text. |

## Using a skill

Make it discoverable by symlinking (or copying) the skills directory into a skills path — e.g. globally:

```sh
ln -s ~/dev/skills ~/.agents/skills
```
