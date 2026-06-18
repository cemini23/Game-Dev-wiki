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

**Status:** Executed through story-029 — next: story-030 playtest parity + optional MCP expand

- Planner: `claude-opus-4-8-thinking-high` (Fable slot when available)
- Executor: `gpt-5.3-codex` swarm per subsystem
- Verifier: playtest gate + `wiki_lint.py` + regression scene
- Steal role graph from `@ccc-wiki/entities/tools/claude-code-game-studios.md`

### W3 — Art pipeline (parallel, low priority)

Cross-link `@image-gen-wiki` for isometric tile/sprites; `@concepts/art-pipeline-v0-requirements.md` stub in place.

### W5 — Stronghold 2 clone research (operator north star)

**Status:** Active — mechanics mapped; building/unit deep-read pending

- [x] Operator vision + legal boundary documented
- [x] SH2 systems inventory (honour, crime, kingmaker, popularity, modes)
- [x] GDD phase ladder in `briefs/GDD-sh2-personal-clone.md`
- [ ] Operator playtest notes — **closed YouTube path** → `briefs/story-030-sh2-playtest-parity.md`
- [x] Deep SH2 research batch — Exa + Heaven + YouTube dev interviews → @sources/sh2-exa-youtube-deep-research-2026-06-17.md
- [x] Kingmaker strategy, siege warfare, estates concept pages
- [x] SH2 Heaven military units + campaign walkthrough follow-up (2026-06-17)
- [x] SH2 second pass — PoW roster, castle structures, Kingmaker ranks, Nation/Fandom AI lords (2026-06-18)
- [ ] Ingest SH2 Heaven per-industry building stat pages (civilian/farm partial)
- [x] Production building cost tables → @concepts/stronghold-2-production-buildings.md (2026-06-18)
- [x] LordProfile.json stub in castle-sim → `data/sh2/lord_profiles.json`
- [x] SH2 mod ecosystem scan (ModDB/Nexus/YouTube/GitHub) → @concepts/stronghold-2-mod-ecosystem-shelf.md (2026-06-18)
- [x] Visual QoL presets + Nevikov balance sheet → @concepts/stronghold-2-visual-qol-presets.md, `balance_presets.json`, `graphics_presets.json` (2026-06-18)
- [x] Decide **D4** fork: 2D mechanics (A) vs 3D rebuild (B) vs 2.5D (C) → **B locked 2026-06-13**
- [x] **M0.3D architect spike** — `briefs/story-005-3d-architect-spike.md` — PROCEED + operator perf PASS (story-029)

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
- [x] Port CCGS P0 skills checklist into `briefs/WORKFLOW.md` at W2 kickoff
- [x] Evaluate godot-stagehand for castle-sim CI smoke tests → research in `wiki/concepts/godot-stagehand-ci-smoke-plan.md`
- [x] Ingest GDC Vault transcripts (K&C, Total War siege) — K&C summary deepened; TW siege ingested from GDC blurb + forum recap
- [x] Shaggydev / papierkorp Godot RTS devlogs as sources
- [x] Tool Evaluation cross-wiki batch (56 targets, docx) → concepts + 4 entities + routing stubs
- [x] Phase-0 audit SerpentAI, Airtest, UCP2 + W2 briefs (story-003/004, harness kickoff)
- [x] Phase-0 audit SH2 AnalyseHub, MP-AI patch, GameDev-Resources (2026-06-16)
- [x] Inbox arXiv reject batch triaged + archived to egress (2026-06-16)
- [x] Inbox re-drop triage (2026-06-17) — 5 PDFs re-archived, no new concepts
- [ ] Route isometric tile workflow to `@image-gen-wiki` when art milestone starts
- [ ] Deploy cross-wiki stubs (SerpentAI, Airtest, UCP2, GameDev-Resources) to sibling wikis

---

## Open decisions

| ID | Question | Default if no answer |
|----|----------|---------------------|
| D1 | 2D isometric vs simplified 3D | **2D isometric** (Stronghold 1 vibe, lower art cost) |
| D2 | Real-time MP vs hot-seat/LAN first | **Hot-seat / solo** until slice playable |
| D3 | `castle-sim` repo public? | **Private** until vertical slice demo |
| D4 | SH2 clone presentation fork | **Fork B — Godot 3D** (2026-06-13). Spike: @concepts/godot-3d-sh2-architect-spike-plan.md |

---

## Done log

### 2026-06-13 — W4 devlog + GDC + harness workflow research

- Shaggydev + papierkorp pathfinding devlogs; TW siege GDC shelf; stagehand CI plan
- `briefs/WORKFLOW.md` (local) for W2 Codex stories

### 2026-06-13 — W1 complete + Stronghold research

- Franchise inventory + SH1 systems deep-dive; sources ingested (HD manual, Wikipedia)
- `castle-sim` scaffolded; sibling wiki inventory; art pipeline v0 stub
- ROADMAP W1 closed; W2 ready for pathfinding spike

### 2026-06-13 — K115 bootstrap

- Federation wiki `game-dev-wiki` created; GitHub public repo; digest + sync wired
