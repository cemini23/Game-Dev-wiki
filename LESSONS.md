# LESSONS — Game Dev Wiki

Meta-lessons about **how we work** on this hobby project.

## L1 — Wiki before repo (2026-06-13)

**Lesson:** For multi-year solo + agent-assisted game dev, the wiki is the **memory layer**. Scope cuts, engine decisions, and harness failures must be written down before spinning up `castle-sim` code — otherwise every new agent session re-litigates Stronghold scope.

## L2 — One subsystem per swarm (2026-06-13)

**Lesson:** "One-shot full RTS" demos are vertical slices with hidden scope cuts. Codex swarms should receive **one milestone** (e.g. grid wall placement only) with acceptance tests. Planner writes slice spec in wiki first; executor never owns scope.

## L3 — Harness lives in CCC, game-specific in this wiki (2026-06-13)

Generic subagent orchestration → `@ccc-wiki`. Castle-project model matrix, milestone gates, playtest rituals → here. Cross-link both ways; don't fork harness docs.

## L4 — Fable is optional planner slot (2026-06-13)

Fable 5 withdrawn from Cursor subagents 2026-06-13. Opus plans now; swap planner model when Fable returns without changing wiki structure.
