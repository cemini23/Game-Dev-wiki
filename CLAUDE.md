# Game Development Research Wiki — Schema

This file is the **schema**: it tells you (the LLM) how to operate this workspace. Everything else is either a raw source, a wiki page, or a meta file. Read this on every session start. Active workstreams + open decisions live in `ROADMAP.md`, not here.

## Purpose

Local knowledge hub for **hobby game development** — scoped to:

1. **Castle / RTS / simulation design** — Stronghold-inspired castle building, economy, siege, AI (research + vertical slices).
2. **Engine & tooling evals** — Godot, Unity, Bevy, asset pipelines; Phase-0 audits before adoption.
3. **Agent-assisted dev harness** — plan (Opus/Fable) → execute (Codex swarm) → verify; role graphs, milestone gates.
4. **Art & audio pipeline** — 2D isometric tiles, sprites, procedural placeholders; cross-link `@image-gen-wiki` for generation workflows.
5. **Multiplayer (later)** — lockstep/deterministic RTS notes; LAN/hot-seat before real-time online.

The wiki is a librarian that **manages, curates, and applies** that knowledge:

- **Manage** — inventory tutorials, GDC notes, engine docs, agent workflow posts; track read status
- **Curate** — interlinked pages on concepts, engines, tools, games (reference titles), and harness patterns
- **Apply** — route findings to `briefs/` and future `game-projects/` repos (code stays out of this public wiki)

Laptop-first workspace. Raw sources archive to **`cemini-egress-fi:/opt/cemini-bulk/research/game-dev/`** via OSINT `archive_raw_to_egress.sh`. Librarian rsync **decommissioned 2026-06** (see `@osint-wiki/meta/librarian-decommission-2026-06-14.md`).

## Scope boundary — vs sibling wikis

| Topic | **This wiki (`game-dev-wiki`)** | **Sibling** |
|-------|----------------------------------|-------------|
| Castle sim design, Godot RTS slices | **Primary home** | — |
| Agent orchestration (subagents, swarms, harness) | Requirements + game-specific harness | **@ccc-wiki** primary |
| AI art / sprite generation | Pipeline notes + links | **@image-gen-wiki** primary |
| CeminiSuite / trading / PM bots | Out of scope | **@osint-wiki** |
| Poker / dev.fun arena bot | Out of scope | **@gambling-wiki** + private osint agents |

**Routing rule:** ingest here when the source teaches *how to build or design a game* or *how to run agent-assisted game dev*. Route harness primitives to `@ccc-wiki` stubs. Route pure image-gen technique to `@image-gen-wiki`.

**Code boundary:** runnable game repos are **gitignored** under `game-projects/` except `README.md` pointer. Public wiki holds design + research only.

## Architecture — three layers

1. **Raw sources** — immutable. Canonical archive: `cemini-egress-fi:/opt/cemini-bulk/research/game-dev/` via OSINT `archive_raw_to_egress.sh`
2. **The wiki** — LLM-written, human-read. `wiki/`
3. **The schema** — this file

Staging:
- `briefs/` — milestone specs, slice briefs (gitignored)
- `research to be indexed/` — transient drop zone (gitignored)
- `LESSONS.md`, `ROADMAP.md`, `hot.md` (gitignored)

## Folder layout

```
Game Dev wiki/
  CLAUDE.md
  LESSONS.md
  ROADMAP.md
  game-projects/README.md       # pointers to implementation repos (code gitignored)
  wiki/
    index.md
    log.md
    sources/
    entities/
      engines/                  # Godot, Unity, Bevy, …
      tools/                    # building kits, pathfinding libs, agent harness refs
      games/                    # reference titles (Stronghold, …)
    concepts/                   # scope tiers, deconstruction, harness, slice specs
    meta/                       # cadence, cross-wiki routing
    sweeps/                     # daily digest reports
  scripts/
  prompts/
```

## Wiki page format

Same as Cemini federation standard — YAML frontmatter + `## Relations`, `## Raw Concept`, `## Narrative`, optional `## Snippets`, `## Dead Ends`.

Claim tags: `[CONFIRMED]`, `[TENTATIVE]`, `[NEEDS VERIFICATION YYYY-MM-DD]`, `[RETRACTED]`.

## Operations

### Ingest

1. Drop source → `research to be indexed/`
2. `python3 scripts/preingest_check.py`
3. Discuss takeaways with operator before writing
4. Cross-wiki routing check → `python3 scripts/cross_wiki_route.py` from OSINT if needed
5. Create `wiki/sources/<slug>.md`; update concepts/entities; bidirectional `related:`
6. Update `wiki/index.md`, append `wiki/log.md`
7. Archive large PDFs: `bash "../../OSINT WORKSPACE/scripts/archive_raw_to_egress.sh" --wiki-id game-dev "<file>"`; `python3 scripts/wiki_lint.py`
8. Bump `ROADMAP.md` when milestone shifts

### Phase-0 (engines/tools)

Before adopting an engine or third-party kit: clone to `/tmp/<tool>-audit/`, license + maturity + failure-mode audit, GO/CONDITIONAL-GO/NO-GO on entity page. Same pattern as `@osint-wiki` Phase-0.

### Query

Read `wiki/index.md` → follow `@relations`. File synthesis back to wiki if valuable.

### Session-start ritual

1. Read `hot.md` if present (gitignored)
2. Check latest `wiki/sweeps/*-daily.md` if digest enabled
3. Check `research to be indexed/` for inbox items
4. Read `ROADMAP.md` for active milestone

## Related Wikis

| Alias | Path | Visibility | Description |
|-------|------|------------|-------------|
| `game-dev-wiki` | `wiki/` | **Public** | Hobby game dev, castle/RTS research, engine evals, agent-assisted slice workflow |
| `osint-wiki` | `../../OSINT WORKSPACE/wiki/` | **Private** | Quant finance, CeminiSuite, federation sync scripts |
| `ccc-wiki` | `../Cemini claude code CCC/wiki/` | **Public** | Agent orchestration, subagents, harness, eval prompts |
| `image-gen-wiki` | `../Image gen/wiki/` | Public | Sprites, tiles, ComfyUI — art pipeline for games |
| `gambling-wiki` | `../Gambling wiki/wiki/` | Public | Minimal overlap (dev.fun poker bot stays there) |
| `cybersecurity-wiki` | `../Cybersecurity wiki/wiki/` | Public | Minimal overlap |
| `seo-wiki` | `../SEO:GEO B&M Business/wiki/` | Public | Minimal overlap |
| `3d-printing-wiki` | `../3D printing/wiki/` | Public | Physical props only |

### Raw archive (federation)

```bash
bash "../../OSINT WORKSPACE/scripts/archive_raw_to_egress.sh" --wiki-id game-dev "research to be indexed/<file>"
```

Wiki canon stays on laptop git — no kb-server sync.
