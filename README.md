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

## Latest highlights (as of 2026-11-12)

- **MiniMax H3-Image** — Open-weight native 4K (16MP) T2I + multi-ref editing in <10s; rising to top of HF trending; community license (excludes some regions).
- **Baidu ERNIE 5.5 Flash Preview** — 280B/14B active MoE, 1M context, strong coding/3D; API live; weights Apache 2.0 by Nov 25.
- **Alibaba Qwen4-Max-Preview** — Multimodal flagship (text/image/video), 1M context, reasoning + tools; Token Plan preview until Nov 25; no weights yet.
- **DeepMind AlphaGenome 2** — Cell-type-specific DNA variant prediction; nearly 2x causal variants; free non-commercial API.
- **Ongoing frontier** — Claude Fable 5.2 tops AA Index (65) at $8/$40; Gemini 4 Carbon GA at intro $2/$10. LongCat-2.5 full MIT open weights.
- **Trending HF** — MiniMax-H3-Image, uncensored DeepSeek, idol (image-to-3D), Arete-27B, Kimi K3.1 Pro, LTX-2.5, Ripple-65B.
- **Free APIs / GPUs** — Stable free tiers on Kaggle (~30h/week), Colab, HF ZeroGPU, Lightning/Modal credits, NVIDIA NIM, Groq, Gemini AI Studio, OpenRouter, Cloudflare. AMD MI300X credits.

See [CURRENT.md](CURRENT.md) for the full snapshot.
