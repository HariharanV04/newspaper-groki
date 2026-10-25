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

## Latest highlights (as of 2026-10-25)

- **Microsoft Agensh** — open-sourced decentralized harness scaling to 1,024 self-organizing coding agents (MIT)
- **Block Dessa** — full-duplex speech-to-speech model trained only on human conversation (local on M4 Max; research preview)
- **Moonshot Kimi K3.1 Pro** — near-frontier 2.8T/104B MoE (1M context); open weights due Nov 4
- **NVIDIA Nemotron 3.5 Bolt E4B** — open 4GB local conversational agent / NPC model
- **HF Carbon-X** — open 14B model for chatting with DNA sequences
- **Recursive Flint** — 40B MoE laptop coding model; MiniMax M3.1 Flash weights public
- Diffusers 0.42.0 with FLUX.3, Fibo 2.0, Kandinsky 6

See [CURRENT.md](CURRENT.md) for the full snapshot.
