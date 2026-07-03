# skill-smith

Meta-skill that creates, refines, and reviews the other skills in this repo through a grill-style design interview and a quality checklist.

## Usage

Triggers when the user wants a new personal skill built ("make me a skill that…"), an existing one improved ("improve the handoff skill"), or a skill reviewed against best practices. The argument describes the new skill — or names an existing one to edit.

## What it does

- Detects create vs edit mode from the argument and confirms it
- Gates new ideas first: some belong in CLAUDE.md or a shell alias, not a skill
- Interviews using the sibling `grill-me` method — batched questions with recommended answers — to pin down invocation mode, trigger, flow, and output before writing
- In edit mode, diagnoses the existing skill against known failure modes (sediment, sprawl, duplication, no-ops) before applying the change
- Drafts against vendored best-practice references (Matt Pocock's *writing-great-skills*, MIT) and 1–2 sibling skills as house-style exemplars
- Finishes with a quality-checklist review, README updates, and offers to symlink-install and commit
