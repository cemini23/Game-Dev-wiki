# Game Development Wiki

> A public knowledge hub for **hobby game development** — castle/RTS research, engine evals, and agent-assisted slice workflow. LLM-managed, human-read. Welcome in.

## What this is

This workspace is a **librarian** for a long-horizon personal game project (Stronghold-inspired castle sim). It:

- **Manages** raw sources — tutorials, GDC notes, engine docs, agent workflow posts
- **Curates** interlinked wiki pages — scope, deconstruction, harness, engines, tools
- **Applies** findings via local `briefs/` and a separate implementation repo under `game-projects/`

**Game source code does not live in this public repo.** See [`game-projects/README.md`](game-projects/README.md).

## Quick start

1. Read [`CLAUDE.md`](CLAUDE.md) — schema the LLM follows each session
2. Read [`ROADMAP.md`](ROADMAP.md) — active workstreams (Phase 0 research complete; implementation in `castle-sim`)
3. Browse [`wiki/index.md`](wiki/index.md) — page catalog
4. Copy `.env.example` → `.env` (optional Exa/Brave keys for the daily digest)
5. Drop a source into `research to be indexed/` and ask Cursor to ingest
6. Lint: `python3 scripts/wiki_lint.py`

**CI (GitHub):** wiki lint on push — `python3 scripts/wiki_lint.py --fail-on-dangling`

## Folder layout

```
Game Dev wiki/
  CLAUDE.md
  README.md
  ROADMAP.md
  LESSONS.md
  game-projects/README.md     # pointers only — code in separate repos
  wiki/
    index.md
    log.md
    concepts/                 # scope, Stronghold deconstruction, harness, slices
    entities/engines/         # Godot, …
    entities/tools/
    entities/games/           # reference titles
    entities/projects/        # castle-sim pointer, …
    sources/
    meta/
    sweeps/
  scripts/
  prompts/
```

## Cemini wiki federation

**Eight** interlinked markdown wikis plus private **Cemini Financial Suite**. Cross-links use `@<alias>/path/to/page.md` (see `CLAUDE.md` → Related Wikis).

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

- `.env`, `raw-sources/`, `research to be indexed/`, `briefs/`, `hot.md`, and `game-projects/*` (except this README) are gitignored
- Never commit API keys or unreleased asset binaries

## Related

- Methodology newsletter: [Outlier Weekly](https://outlierweekly.substack.com)
- YouTube: [@Cemini23](https://www.youtube.com/@Cemini23)
- Agent harness patterns: `@ccc-wiki/entities/tools/claude-code-game-studios.md`
- Federation hub: [cemini-claude-code-CCC](https://github.com/cemini23/cemini-claude-code-CCC)
- Tooling: [wikilint](https://github.com/cemini23/wikilint) · [vet](https://github.com/cemini23/vet)

## Support

Thank you for visiting — and thank you to everyone who supports this work. Tips and attention help keep the public wikis, research, and tooling open.

Voluntary tips fund open research and tooling. **Donation-only addresses** — not trading or production wallets.

| Chain family | Address |
|--------------|---------|
| **X Money** (fiat, US) | Request [@Cemini23](https://x.com/Cemini23) in the X app — scan the Request QR |
| **EVM** (Ethereum, Polygon, Base, Arbitrum, …) | `0x444C5C2eC439E0382aa5a17F70313c536BcC5D58` |
| **Solana / SVM** | `J4zNn4hK9jTrKBFY8sbAGJHLoZvXvQf4B9pQSbSrocZE` |
| **Polymarket** (referral) | [polymarket.com/?r=Cemini23](https://polymarket.com/?r=Cemini23) |

**Projects & sites**

| Project | Link |
|---------|------|
| **Outlier Weekly** (methodology newsletter) | [outlierweekly.substack.com](https://outlierweekly.substack.com) |
| **Atto** (genealogy kit) | [youratto.com](https://youratto.com) |
| **GuruWatcher** (newsletter price watches → Discord) | [guruwatcher.com](https://guruwatcher.com) |
| YouTube | [@Cemini23](https://www.youtube.com/@Cemini23) |

## License

MIT — see [`LICENSE`](LICENSE).
