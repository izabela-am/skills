# study-tutor

A personal Socratic study tutor for Claude Code, optimized for **durable understanding,
not fast completion**. It teaches by asking, verifies learning with a transfer-based
explain-back gate, and maintains your study state on disk itself — no copy-paste loop,
no manual note-keeping.

## What makes it different from "just asking Claude to teach me"

- **Socratic by default, with a primer floor.** It draws out your reasoning with targeted
  questions instead of lecturing — but never interrogates you on things you have no way of
  knowing yet. Brand-new topics get a brief primer first.
- **Knowledge as a dependency graph.** Curricula annotate every topic with `deps:`. On a
  new subject the tutor runs **placement**: it probes topics in dependency order, prunes
  the dependents of anything you fail, and places you at the first failure whose
  prerequisites all passed — instead of starting from lesson one.
- **A gate that can't be talked past.** Before advancing, you explain the concept back
  *and* apply it to a novel instance (predict what breaks, produce a counterexample).
  A fluent paraphrase doesn't count as understanding.
- **Debt is tracked, never hidden.** You can always choose momentum and defer a topic,
  but the tutor records it and warns you before building anything on top of it.
- **Decay-aware resume.** Passes older than ~6–8 weeks go stale; on resume the tutor
  spot-checks only the stale prerequisites of what you're about to study next.
- **Escalating hints.** Nudge → key insight → full answer, and the full answer only after
  a genuine attempt and an explicit ask.

## Where your study state lives

State is **not** stored in this skill directory. It lives in a separate git repo at:

```
~/dev/study-sessions/
  index.md                 # active subjects + shaky/deferred/stale rollup
  subjects/<subject>/
    curriculum.md          # topics, deps, per-topic status, placement verdict
    progress.md            # session log, newest first
    progress-archive.md    # rotated old entries
    flashcards.md          # insight/gotcha cards
```

Keeping state in its own repo means it survives skill updates, is versioned by you, and
is portable — clone `~/dev/study-sessions` on each machine you study from. The tutor
writes state changes live during a session but **never commits**; you commit when you
want a checkpoint.

Older versions of the skill stored state inside the skill directory itself. The tutor
detects that and migrates it into the repo per subject the first time you touch a
subject, asking you to reconcile if both copies have history.

## What ships in this directory

These are read-only skill assets, not study state:

| File | Purpose |
|------|---------|
| `SKILL.md` | The tutor's full instructions (method, gates, state protocol). |
| `curriculum-template.md` | Blank template for authoring a new subject's curriculum. |
| `index-template.md` | Format reference for the state repo's `index.md`. |
| `starters/dsa/` | Prebuilt Data Structures & Algorithms curriculum to seed a new subject from. |
| `how-to.md` | Human-friendly cheat sheet of the commands below. |

## Install

Symlink (or copy) this directory into a Claude Code skills path:

```sh
ln -s "$PWD/study-tutor" ~/.claude/skills/study-tutor
```

Then invoke it as `/study-tutor`, or just say something it matches naturally
("studying X", "quiz me", "new topic").

## Usage

Start a session:

- **"New topic: X, I'm a beginner"** — primer first, then Socratic.
- **"Plan a curriculum for X"** — drafts topics + dependencies with you (or seeds from a
  starter if one exists), saved to the state repo. Required before placement can run.
- **"Studying X, we left off at Y"** — resumes: reads the curriculum and the latest
  progress entry, confirms where it's picking up, then continues.
- **"I've got 20 minutes"** — scopes the session upfront.

Steer mid-session:

- **"Hint" → "bigger hint" → "show me the answer"** — escalating help.
- **"Just explain this one"** / **"go deeper"** / **"slow down"** — adjust depth.
- **"Quiz me"** / **"let me explain it back"** — trigger the gate yourself.
- **"Make me a flashcard"** — capture a transfer insight or gotcha.

End and maintain:

- **"Wrap up" / "log this"** — writes the progress entry, updates the index, suggests a commit.
- **"What's still shaky?"** — weekly review of shaky, deferred, and stale topics across
  all subjects.

The full command list lives in [`how-to.md`](how-to.md).
