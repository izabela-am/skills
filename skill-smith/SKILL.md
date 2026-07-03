---
name: skill-smith
description: Create, refine, and review the user's personal Claude Code skills through a grill-style design interview and a quality checklist. Use when the user wants a new personal skill built ("make me a skill that…"), an existing one improved ("improve the handoff skill"), or a skill reviewed against best practices.
argument-hint: "What should the new skill do — or which existing skill to improve?"
---

# Skill Smith

You create and refine the user's personal skills. The skills repo is the parent directory of this skill's own directory — resolve it from wherever this SKILL.md lives, following symlinks (normally `~/dev/skills`). If this skill is running from somewhere that isn't that repo — e.g. a plugin cache — target `~/dev/skills` directly. Everything you write lands in that repo, never in a company plugin repo — `~/dev/skills` is the canonical home of these skills; the copy under ai-plugins is a deployment mirror, refreshed manually by copy + PR.

Read [references/WRITING-GREAT-SKILLS.md](references/WRITING-GREAT-SKILLS.md) before drafting or diagnosing — it is the design vocabulary (invocation loads, information hierarchy, leading words, pruning, failure modes) this skill assumes.

## Detect the mode

List the repo's skill directories, then check whether the argument refers to one of them — by exact name or in natural language ("improve the handoff skill" refers to `handoff/`). If it does, enter **edit mode**; otherwise **create mode**. State the detected mode and, in edit mode, the matched skill in your first response so the user can correct it.

## Create mode

### 1. Gate

Before designing anything, check the idea deserves to be a skill:

- Is it a recurring workflow, not a one-off prompt?
- Does it need instructions beyond a sentence? A standing preference belongs in CLAUDE.md; a purely mechanical command belongs in a shell alias.
- Is it worth the load it costs — context load if model-invoked, cognitive load if user-invoked?

If it fails the gate, recommend the better home and stop. Done when: the idea passes, or the user has heard the better home and still wants a skill.

### 2. Interview

Interview using the method in the sibling skill `../grill-me/SKILL.md` — read it and apply it. If the sibling is missing, fall back to its core: interview relentlessly, walk each branch of the design tree, resolve dependencies one by one, recommend an answer for every question, and explore files instead of asking when they can answer.

Deliver questions in small batches — 2–4 related questions per round, one design branch per round, each with a recommended answer.

Pin down at minimum:

- **Invocation** — model-invoked (trigger-rich description) or user-invoked (`disable-model-invocation: true`, human-facing description)? Use the trade-off in the reference.
- **Trigger** — what the skill does and exactly when it should fire.
- **Flow** — the steps, each ending on a checkable completion criterion.
- **Output** — what exists when a run has succeeded.

Structure decisions (single vs multi-file, what to disclose to `references/`, templates, on-disk state) are yours to make with sensible defaults from the reference — surface one only when it genuinely changes what the user gets.

Done when: you can state the whole design in one summary and the user confirms it.

### 3. Draft

Read one or two sibling skills as house-style exemplars before writing. Then write the skill directory, applying the reference: lean SKILL.md, reference material disclosed behind pointers only when it earns the move, leading words over restatement, every sentence surviving the no-op test.

Done when: every file in the confirmed design exists on disk.

## Edit mode

1. Read the target skill in full, including its references.
2. Diagnose it against the failure modes in the reference — sediment, sprawl, duplication, no-ops, premature completion — and report what you find.
3. Grill only about the requested change and anything it destabilises, same batched style as create mode.
4. Apply the change.

Done when: the requested change is in and the diagnosis findings are either fixed or explicitly deferred by the user.

## Finish (both modes)

1. Review the result against every item in [references/CHECKLIST.md](references/CHECKLIST.md); fix failures. Done when every item passes or the user waives it.
2. Write or update the skill's own README.md, matching the sibling READMEs (one-line summary, Usage, What it does).
3. Add or update the skill's row in the repo README table.
4. Offer to symlink the skill into `~/.claude/skills/` (create the directory if needed) so it is usable immediately.
5. Offer to commit and push, following the user's git conventions — no AI attribution anywhere.
