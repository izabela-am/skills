# handoff

Compact the current conversation into a handoff document so another agent can pick up the work.

## Usage

Triggers when the user wants to hand off the current session. Optional argument describes what the next session will focus on.

## What it does

- Writes a handoff doc to the OS temp directory (not the workspace)
- Includes a "suggested skills" section pointing the next agent at the right tools
- References existing artifacts (PRDs, plans, ADRs, issues, commits, diffs) by path or URL instead of duplicating them
- Redacts secrets and PII before saving
- Tailors the doc to any user-provided description of next-session focus
