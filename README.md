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

## Latest highlights (as of 2026-11-17)

- **Alibaba Qwen4-Max** — Full launch: new MoE (~2.4T/71B active), native vision, 1M context, $1.50/$4.50. Efficiency claims for long-horizon work; smaller open weights planned.
- **Tencent Hy4 flash** — Ultra-low-cost multimodal MoE (224B total / 12B active, 1M context) at $0.07/$0.281 per M tokens.
- **Meituan LongCat-Video-Avatar 1.6** — MIT open weights for improved audio-driven human video generation (better lip sync, motion, long videos).
- **Unsloth Dynamic V3.1 GGUFs for Qwen3.8-27B** — 5–10% accuracy gains on Terminal Bench, DeepSWE and more vs prior quants; runnable on 12GB RAM.
- **Inkling 2 Small weights live** — Thinking Machines open multimodal MoE under Apache 2.0 on HF with day-0 serving support.
- **MiniMax H3-Image** — Continues top HF trending: native 4K T2I + multi-ref editing, open weights.
- **Gemini 4 Hydrogen** — Google’s fast agentic model widely available incl. free tiers.
- **Trending HF** — Uncensored DeepSeek variants leading, MiniMax-H3-Image, Qwen3.8-27B, LTX-2.5, Inkling-2-Small, ZONOS3-Mini, idol.
- **Free APIs / GPUs** — Kaggle (~30h/week more predictable), Colab T4, Modal ($30/mo), E2B ($100), HF ZeroGPU, Lightning credits, NVIDIA Build, Groq, Gemini AI Studio (incl. Hydrogen), OpenRouter (free Ling-3.2-flash 1M), Cloudflare. AMD MI300X credits.

See [CURRENT.md](CURRENT.md) for the full snapshot.
