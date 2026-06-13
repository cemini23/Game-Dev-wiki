# Game Dev Wiki — ROADMAP

Active workstreams, open decisions, and done log.

---

## Vision

Build a **playable castle-sim vertical slice** (Stronghold-inspired, 2D isometric, solo + optional friends) over a multi-year hobby timeline. This wiki holds **research + design + agent harness**; code lands in a separate repo when Phase 0 completes.

## Active workstreams

### W1 — Wiki bootstrap + Phase 0 research (2026-06-13)

**Status:** Complete — handoff to implementation spike

- [x] Scaffold repo from Gambling-wiki / Cybersecurity-wiki federation pattern
- [x] Seed concept pages (scope, Stronghold deconstruction, vertical slice v0, agent harness)
- [x] Wire federation (sync, daily digest, hub paths, OSINT pointer)
- [x] Godot 4 Phase-0 deep-read + GO/NO-GO on entity page → **CONDITIONAL-GO**
- [x] Ingest Stronghold franchise research (HD manual + Wikipedia + systems inventory)
- [x] Lock vertical slice v0 acceptance criteria (spike gate + playtest script)
- [x] Scaffold `castle-sim` implementation repo → `/Users/claudiobarone/Desktop/projects/castle-sim/`
- [x] Sibling wiki inventory (ccc, image-gen, cybersec cross-links)

### W2 — Agent harness pilot (after slice spec locked)

**Status:** Ready — run on pathfinding spike in `castle-sim`

- Planner: `claude-opus-4-8-thinking-high` (Fable slot when available)
- Executor: `gpt-5.3-codex` swarm per subsystem
- Verifier: playtest gate + `wiki_lint.py` + regression scene
- Steal role graph from `@ccc-wiki/entities/tools/claude-code-game-studios.md`

### W3 — Art pipeline (parallel, low priority)

Cross-link `@image-gen-wiki` for isometric tile/sprites; `@concepts/art-pipeline-v0-requirements.md` stub in place.

### W4 — Ongoing research ingest

**Status:** Active (2026-06-13 Exa batch)

- [x] Exa deep batch (10 clusters, 71 URLs) → 6 concepts + 8 sources
- [x] Exa flow-fields + Firefly batch (8 clusters, 68 URLs) → flow-field concept + 8 sources
- [x] Exa AI game-dev tools batch (10 clusters, 81 URLs) → general AI workflow + tool stack
- [x] Exa NPC + PCG + CCGS batch (11 clusters, 82 URLs) → runtime NPC shelf, agentic PCG, CCGS extraction
- [x] Tighten daily digest paper queries (game-specific, less UAV noise)
- [x] Phase-0 audit hi-godot/godot-ai → **CONDITIONAL-GO** W2
- [x] Phase-0 audit Sods2/godot-mcp → **CONDITIONAL-GO** W2 alt
- [x] Phase-0 audit godot-stagehand + godot-ai-playtest → **CONDITIONAL-GO** W2
- [x] Phase-0 audit Claude-Code-Game-Studios → **STEAL-FROM** (patterns only)
- [ ] Port CCGS P0 skills checklist into `briefs/WORKFLOW.md` at W2 kickoff
- [ ] Evaluate godot-stagehand for castle-sim CI smoke tests
- [ ] Ingest GDC Vault transcripts (K&C, Total War siege) when slice needs them
- [ ] Shaggydev / papierkorp Godot RTS devlogs as sources
- [ ] Route isometric tile workflow to `@image-gen-wiki` when art milestone starts

---

## Open decisions

| ID | Question | Default if no answer |
|----|----------|---------------------|
| D1 | 2D isometric vs simplified 3D | **2D isometric** (Stronghold 1 vibe, lower art cost) |
| D2 | Real-time MP vs hot-seat/LAN first | **Hot-seat / solo** until slice playable |
| D3 | `castle-sim` repo public? | **Private** until vertical slice demo |

---

## Done log

### 2026-06-13 — W1 complete + Stronghold research

- Franchise inventory + SH1 systems deep-dive; sources ingested (HD manual, Wikipedia)
- `castle-sim` scaffolded; sibling wiki inventory; art pipeline v0 stub
- ROADMAP W1 closed; W2 ready for pathfinding spike

### 2026-06-13 — K115 bootstrap

- Federation wiki `game-dev-wiki` created; GitHub public repo; digest + sync wired
