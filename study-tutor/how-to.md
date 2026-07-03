# How to Use My Study Tutor — Cheat Sheet

Quick reference for you. The tutor already knows these commands (they're embedded in
`SKILL.md`) — this file is just a human-friendly reminder. **No copy-paste or re-upload:**
the tutor reads and writes its own state in the `~/dev/study-sessions/` repo
(`index.md` + `subjects/<subject>/`), separate from this skill directory.

## Starting a session
- **"Studying [subject], we left off at [X]"** — resume. The tutor reads the subject's
  `curriculum.md` + latest progress, confirms where it's picking up, then continues.
- **"New topic: [X], I'm a beginner"** — triggers a primer before Socratic mode.
- **"I've got 20 minutes"** — scopes the session (planning input, not a live timer).
- **"Help me plan a curriculum for [X]"** — fills a curriculum from `curriculum-template.md`
  (or seeds from a `starters/<subject>/` if the skill ships one), saved to
  `~/dev/study-sessions/subjects/[x]/curriculum.md` with dependency-annotated topics.

## Steering depth
- **"Just explain this one"** / **"Stop asking, tell me"** — drop Socratic for this bit.
- **"Go deeper" / "first principles"** — push past the surface.
- **"Slow down" / "primer please"** — foundation first.

## When you're stuck
- **"Hint" → "Bigger hint" → "Show me the answer"** — escalating; the answer comes after you've tried.

## Checking understanding
- **"Quiz me."** / **"Let me explain it back."** — the transfer gate (apply it, don't just restate).
- **"Make me a flashcard for this."** — captures an insight card in `flashcards.md`.

## Ending a session
- **"Wrap up" / "log this"** — the tutor writes the progress entry, updates the index, and
  suggests a commit. (Commit yourself when you want a checkpoint — the tutor never auto-commits.)

## Maintenance habits
- Every week or so: **"What's still shaky across everything?"** — targeted review from `index.md`.
- `git commit` in `~/dev/study-sessions/` after sessions you want to checkpoint — the state
  repo is yours to version (the tutor suggests commits but never makes them).
