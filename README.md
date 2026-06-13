# Game Development Wiki

> Public knowledge hub for **hobby game development** — castle/RTS research, engine evals, agent-assisted slice workflow. LLM-managed, human-read.

## What this is

This workspace is a **librarian** for a long-horizon personal game project (Stronghold-inspired castle sim). It:

- **Manages** raw sources (tutorials, GDC notes, engine docs, agent workflow posts)
- **Curates** interlinked wiki pages — scope, deconstruction, harness, engines, tools
- **Applies** findings via `briefs/` and future implementation repos under `game-projects/`

**Game source code does not live in this public repo.** See `game-projects/README.md`.

## Quick start

1. Read `CLAUDE.md` — schema the LLM follows each session
2. Read `ROADMAP.md` — active workstreams (Phase 0 = research only)
3. Copy `.env.example` → `.env` (optional Exa/Brave keys for daily digest)
4. Drop a source into `research to be indexed/` and ask Cursor to ingest
5. Lint: `python3 scripts/wiki_lint.py`

**CI (GitHub):** wiki lint on push — `python3 scripts/wiki_lint.py --fail-on-dangling`

## Folder layout

```
Game Dev wiki/
  CLAUDE.md
  README.md
  ROADMAP.md
  game-projects/README.md     # pointers only — code in separate repos
  wiki/
    index.md
    log.md
    concepts/                 # scope, Stronghold deconstruction, harness, slices
    entities/engines/         # Godot, …
    entities/tools/
    entities/games/           # reference titles
    sources/
    meta/
    sweeps/
  scripts/
```

## Cemini wiki federation

**Eight** interlinked markdown wikis plus private **Cemini Financial Suite**. Cross-links: `@<alias>/path/to/page.md` (`CLAUDE.md` → Related Wikis).

| Alias | Repository | Focus |
|-------|------------|--------|
| **`game-dev-wiki`** | **This repo** | Castle/RTS hobby dev, engine evals, agent harness |
| `osint-wiki` | *private* ([llm-wiki-by-cemini](https://github.com/cemini23/llm-wiki-by-cemini)) | Quant OSINT, federation sync, CeminiSuite |
| `ccc-wiki` | [cemini-claude-code-CCC](https://github.com/cemini23/cemini-claude-code-CCC) | Agent workflow, MCP, skills, multi-wiki eval |
| `gambling-wiki` | [Gambling-wiki](https://github.com/cemini23/Gambling-wiki) | Sports betting, poker, DFS |
| `cybersecurity-wiki` | [Cybersecurity-wiki](https://github.com/cemini23/Cybersecurity-wiki) | Pentest, SOC |
| `seo-wiki` | [SEO-GEO-B-M-Wiki](https://github.com/cemini23/SEO-GEO-B-M-Wiki) | Local SEO, creator ops |
| `3d-printing-wiki` | [3D-Printing-Wiki](https://github.com/cemini23/3D-Printing-Wiki) | FDM/print farms |
| `image-gen-wiki` | [uncensored-image-gen-wiki](https://github.com/cemini23/uncensored-image-gen-wiki) | ComfyUI, sprites, tiles |

```bash
git clone https://github.com/cemini23/Game-Dev-wiki.git
```

## Privacy

- `.env`, `raw-sources/`, `briefs/`, `hot.md`, and `game-projects/*` (except README) are gitignored
- Never commit API keys or unreleased asset binaries

## Related

- Agent harness patterns: `@ccc-wiki/entities/tools/claude-code-game-studios.md`
- Federation hub: [cemini-claude-code-CCC](https://github.com/cemini23/cemini-claude-code-CCC)
- Tooling: [wikilint](https://github.com/cemini23/wikilint)

## License

MIT — see `LICENSE`.
