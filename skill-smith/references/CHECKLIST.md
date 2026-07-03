# Skill quality checklist

Run every item against the finished skill. Fix what fails; only the user can waive an item.

## Frontmatter

- [ ] `name`: kebab-case, ≤64 chars, matches the directory name
- [ ] Invocation mode deliberately chosen: model-invoked (no `disable-model-invocation`) or user-invoked (`disable-model-invocation: true`)
- [ ] `description`: ≤1024 chars; if model-invoked, states WHAT it does AND WHEN to fire (concrete trigger phrases, one per branch, no synonym duplication), third person; if user-invoked, a human-facing one-liner with trigger lists stripped
- [ ] `argument-hint` present if the skill expects arguments

## Body

- [ ] Instructions address Claude, not the user
- [ ] Self-contained: no dependency on tools, machines, or company infrastructure that won't exist elsewhere; paths repo-relative
- [ ] Progressive disclosure: SKILL.md stays lean; long reference material lives in `references/`, reusable file skeletons in template/asset files
- [ ] Every step ends on a checkable completion criterion (exhaustive where it matters)
- [ ] Every relative link resolves to a real file
- [ ] States what to do when preconditions fail (missing files, wrong directory, absent sibling skill)

## Lean-ness

- [ ] No no-ops: every sentence changes behaviour versus the default
- [ ] Single source of truth: each meaning defined in exactly one place
- [ ] Restated concepts collapsed into leading words where one exists

## Repo integration

- [ ] Row added or updated in the repo README table
- [ ] Per-skill README.md written (human-facing: one-liner, Usage, What it does)
- [ ] House style consistent with sibling skills (checked against 1–2 of them)
