# newspaper-groki

Curated AI news, model releases, research, and developer tools — maintained as **living documents** that get refined, not endless daily files.

## How this repo works

| File / folder | Purpose |
|---------------|---------|
| **[CURRENT.md](CURRENT.md)** | Always the latest full briefing snapshot. Overwritten on each update. |
| **[topics/](topics/)** | Living topic files. New findings are merged in; older entries are refined or marked superseded. |
| **[archive/](archive/)** | Lightweight monthly logs of what changed (deltas only). |

### Topic files

- [topics/models-and-releases.md](topics/models-and-releases.md) — frontier + open-weight models
- [topics/research.md](topics/research.md) — papers and discoveries
- [topics/tools-and-compute.md](topics/tools-and-compute.md) — free GPUs, hosting, inference stacks
- [topics/trends.md](topics/trends.md) — high-level themes

## Update rule (for Grok / maintainers)

1. **Overwrite** `CURRENT.md` with the new full snapshot.
2. **Refine** the relevant `topics/*.md` files in place (edit existing entries; add new ones only when needed).
3. **Append** a short dated delta to the current month’s file under `archive/`.
4. Do **not** create a new dated `.md` for every day.

## Latest highlights (as of 2026-10-24)

- **Moonshot Kimi K3.1 Pro** — near-frontier 2.8T/104B MoE (1M context); AA Index 55 (4th); open weights due Nov 4
- **NVIDIA Nemotron 3.5 Bolt E4B** — open 4GB local conversational agent / NPC model
- **HF Carbon-X** — open 14B model for chatting with DNA sequences (genomics + language)
- **Recursive Flint** — 40B MoE laptop coding model largely built by AI (Eureka Machine)
- **MiniMax M3.1 Flash** — open weights now public (428B/23B, low-cost agents)
- Ongoing: DeepSeek DeepInfer, Voxtral 3, Beam, Muse series, Nemotron, free compute tiers stable

See [CURRENT.md](CURRENT.md) for the full snapshot.
