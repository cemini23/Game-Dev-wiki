# Game Dev Wiki — ROADMAP

Active workstreams, open decisions, and done log.

---

## Vision

Build a **playable castle-sim vertical slice** (Stronghold-inspired, 2D isometric, solo + optional friends) over a multi-year hobby timeline. This wiki holds **research + design + agent harness**; code lands in a separate repo when Phase 0 completes.

## Active workstreams

### W1 — Wiki bootstrap + Phase 0 research (2026-06-13)

**Status:** In progress

- [x] Scaffold repo from Gambling-wiki / Cybersecurity-wiki federation pattern
- [x] Seed concept pages (scope, Stronghold deconstruction, vertical slice v0, agent harness)
- [x] Wire federation (sync, daily digest, hub paths, OSINT pointer)
- [ ] Godot 4 Phase-0 deep-read + GO/NO-GO on entity page
- [ ] Ingest 2–3 Stronghold / RTS GDC or postmortem sources
- [ ] Lock vertical slice v0 acceptance criteria (playable demo definition)
- [ ] Scaffold `castle-sim` implementation repo (private or public TBD)

### W2 — Agent harness pilot (after slice spec locked)

**Status:** Blocked on W1 slice spec

- Planner: `claude-opus-4-8-thinking-high` (Fable slot when available)
- Executor: `gpt-5.3-codex` swarm per subsystem
- Verifier: playtest gate + `wiki_lint.py` + regression scene
- Steal role graph from `@ccc-wiki/entities/tools/claude-code-game-studios.md`

### W3 — Art pipeline (parallel, low priority)

Cross-link `@image-gen-wiki` for isometric tile/sprites; document import path into Godot.

---

## Open decisions

| ID | Question | Default if no answer |
|----|----------|---------------------|
| D1 | 2D isometric vs simplified 3D | **2D isometric** (Stronghold 1 vibe, lower art cost) |
| D2 | Real-time MP vs hot-seat/LAN first | **Hot-seat / solo** until slice playable |
| D3 | `castle-sim` repo public? | **Private** until vertical slice demo |

---

## Done log

### 2026-06-13 — K115 bootstrap

- Federation wiki `game-dev-wiki` created; GitHub public repo; digest + sync wired
