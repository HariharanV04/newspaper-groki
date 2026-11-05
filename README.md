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

## Latest highlights (as of 2026-11-05)

- **Kimi K3.1 Pro** — Open weights released (2.8T / 104B active multimodal MoE, 1M context). Tops Agent Arena among open models; strong agentic coding and long-horizon gains.
- **Ripple-65B Preview** — Dense 65B Apache 2.0 model from RicursiveAI; self-reported US open-weight SOTA on Terminal-Bench 2.1 (80.5) at fraction of larger model cost.
- **OpenAI Images 2.6** — Faster generation, GIFs, SVG, new API models.
- **Trending HF** — Nemotron Transcribe, DeepSeek Flash, Idol, Kimi K3.1 Pro, LFM3-1.7B, Mistral Large 4.
- **Free APIs** — Stable free tiers on Gemini AI Studio, Groq, NVIDIA NIM, Cloudflare Workers AI, Colab, HF ZeroGPU, OpenRouter.
- **Ongoing** — Mistral Large 4 efficiency leadership, llama.cpp FP8, Together inference compiler, agent research on routing and long-horizon reliability.

See [CURRENT.md](CURRENT.md) for the full snapshot.
