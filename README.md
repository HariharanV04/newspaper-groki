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

## Latest highlights (as of 2026-10-15)

- **Lumma-Fev-27B** — FrontiersMind decision model (choices + probabilities)
- **MiniCPM-V 4.7** — first open MoE VLM with strong on-device performance + DSpark heads
- **Gemini 4 Argon** GA — 1M-token frontier model for long-horizon work
- **Meta Muse Wonder** — frontier agent models with Active Memory & Focus
- **LFM2.5-24B-A2B** — open on-device MoE agent model (Liquid AI)
- Free compute stack: Colab, Kaggle, HF ZeroGPU, Lightning, NVIDIA free endpoints

See [CURRENT.md](CURRENT.md) for the full snapshot.