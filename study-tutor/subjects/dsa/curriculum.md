# Curriculum — Data Structures & Algorithms

> The tutor reads and updates this file directly (ticks boxes, edits `status:`).

## Why I'm learning this
Build durable problem-solving fundamentals — recognize which data structure / algorithm a
problem calls for, reason about time & space trade-offs, and write correct solutions under
constraints. Useful for interviews, system-design intuition, and efficient day-to-day code.

## Target outcome
"I know this" =
- Given a novel problem, I can identify the right approach and justify its complexity *before* coding.
- I can implement the core structures/algorithms from scratch without reference.
- I can solve a medium problem end-to-end and explain the trade-offs vs. alternatives.

## Level hypothesis (the tutor verifies this — it does not trust it)
[EDIT ME] — e.g. "comfortable coding, rusty on Big-O and graph algorithms" / "beginner, need
the fundamentals." The tutor probes at the start of each topic and recalibrates from how I answer.

## Placement verdict (the tutor writes this)
_Not yet placed. On the first session the tutor runs graph placement and records the result here._

## Topics
> `id · title` — description `deps:` `status:`.
> deps = ids this builds on (`none` = independent track). status ∈ `unknown | pass (date) | shaky | deferred | fail | stale`.
> Box `[x]` only on `pass`. Independent tracks are probed independently during placement.

**Foundations**
- [ ] **1 · Complexity analysis** — Big-O/Θ/Ω, amortized cost, space vs. time trade-offs. `deps: none` `status: unknown`
- [ ] **2 · Arrays & strings** — two pointers, sliding window, prefix sums. `deps: 1` `status: unknown`
- [ ] **3 · Hashing** — hash maps/sets, collision handling, when hashing beats sorting. `deps: 1` `status: unknown`

**Linear structures**
- [ ] **4 · Linked lists** — singly/doubly, fast/slow pointers, in-place reversal. `deps: 1` `status: unknown`
- [ ] **5 · Stacks & queues** — monotonic stack, deque, their problem patterns. `deps: 1` `status: unknown`
- [ ] **6 · Recursion & backtracking** — recurrence, base cases, pruning the search tree. `deps: 1` `status: unknown`

**Sorting & searching**
- [ ] **7 · Sorting** — merge/quick/heapsort; stability; when to use which. `deps: 1` `status: unknown`
- [ ] **8 · Binary search** — on sorted arrays *and* on the answer space. `deps: 1, 2` `status: unknown`

**Trees & heaps**
- [ ] **9 · Binary trees & BSTs** — DFS/BFS traversals, insertion/lookup invariants. `deps: 1, 6` `status: unknown`
- [ ] **10 · Heaps / priority queues** — heapify, top-K patterns. `deps: 9` `status: unknown`
- [ ] **11 · Tries** — prefix search, autocomplete-style problems. `deps: 2, 9` `status: unknown`

**Graphs**
- [ ] **12 · Graph representations + BFS/DFS** — connectivity, cycle detection, topo sort. `deps: 5, 6` `status: unknown`
- [ ] **13 · Shortest paths** — Dijkstra, BFS on unweighted, when each applies. `deps: 12, 10` `status: unknown`
- [ ] **14 · Union-Find (DSU)** — connected components, Kruskal's MST. `deps: 12` `status: unknown`

**Algorithmic paradigms**
- [ ] **15 · Greedy** — exchange argument, when greedy is provably correct. `deps: 1, 7` `status: unknown`
- [ ] **16 · Dynamic programming** — 1D → 2D, memoization vs. tabulation, state design. `deps: 6` `status: unknown`
- [ ] **17 · Advanced DP** — knapsack family, intervals, DP on trees/graphs. `deps: 16, 12` `status: unknown`

## Milestones
- [ ] Explain Big-O of any solution I write *before* running it.
- [ ] Implement a hash map, a BST, and a min-heap from scratch, no reference.
- [ ] Solve 10 medium problems, each with a stated approach + complexity first.
- [ ] Model a real problem as a graph and pick the right traversal unprompted.
- [ ] Derive the recurrence and state for a DP problem I haven't seen before.

## Resources
- CLRS (*Introduction to Algorithms*) — reference, not cover-to-cover
- *Grokking Algorithms* (Bhargava) — gentle visual intro if starting cold
- NeetCode / LeetCode patterns — practice problems per topic

## Constraints / notes
- Pace: [EDIT ME] e.g. "2 sessions/week, ~45 min each."
- Per topic: primer → Socratic derivation → one from-scratch implementation → one applied problem before `pass`.
- Revisit shaky/deferred items (see `index.md`) at the start of each session.
