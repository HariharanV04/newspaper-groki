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

## Latest highlights (as of 2026-10-18)

- **DeepSeek V4.1-Flash-1017** — MIT open weights, strong agent/coding gains (DeepSWE 77%), faster/shorter outputs, trending #1 on HF
- **Reflection Beam** — 501B sparse MoE open weights, 1M context
- **Meta Muse Spark Open** — 816B/42B multimodal open-weight
- **NVIDIA Nemotron 3.5 Super VL** — 120B/12B open VL for agents + Bolt variants
- Free compute: Colab, Kaggle, ZeroGPU, NVIDIA NIM endpoints, Groq, etc.

See [CURRENT.md](CURRENT.md) for the full snapshot.
