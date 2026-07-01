# skills

Personal Claude Code skills.

| Skill | What it does |
|-------|--------------|
| [`study-tutor`](study-tutor/) | Socratic study tutor — dependency-graph placement, transfer-based explain-back gate, decay-aware recalibration, self-maintained per-subject state on disk. |

## Using a skill

Make it discoverable by symlinking (or copying) the skill directory into a Claude Code
skills path — e.g. globally:

```sh
ln -s "$PWD/study-tutor" ~/.claude/skills/study-tutor
```

Then invoke it as `/study-tutor` (or by natural language matching its description).
