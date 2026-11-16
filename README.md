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

## Latest highlights (as of 2026-11-16)

- **Alibaba Qwen4-Max** — Full launch: new MoE (~2.4T/71B active), native vision, 1M context, $1.50/$4.50. Efficiency claims for long-horizon work; smaller open weights planned.
- **Meituan LongCat-2.5** — MIT open weights (1.6T/~48B active multimodal agent model). Trained on Chinese hardware (no Nvidia). Strong self-reported agent benchmarks; on HF.
- **Claude Fable 5.2 brushstroke imaging** — Generates images via Python-simulated paint strokes (hundreds of thousands) instead of diffusion.
- **GPT-6 Astra** — Credited with leading detailed proof construction for a lattice Standard Model candidate.
- **Unsloth Dynamic V3.1 GGUFs for Qwen3.8-27B** — 5–10% accuracy gains on Terminal Bench, DeepSWE and more vs prior quants; runnable on 12GB RAM.
- **Inkling 2 Small weights live** — Thinking Machines 594B/17B MoE under Apache 2.0 on HF with day-0 serving support.
- **MiniMax H3-Image** — Continues top HF trending: native 4K T2I + multi-ref editing, open weights (community license with regional exclusions).
- **Gemini 4 Hydrogen** — Google’s fast agentic model (1M context, $1.50/$7.50, xhigh thinking); widely available incl. free tiers.
- **Trending HF** — Uncensored DeepSeek variants, MiniMax-H3-Image, Qwen3.8-27B, LTX-2.5, Inkling-2-Small, LongCat-2.5, Arete-27B, Kimi K3.1 Pro, idol.
- **Free APIs / GPUs** — Stable free tiers on Kaggle (~30h/week), Modal ($30/mo), E2B ($100), HF ZeroGPU, Lightning credits, NVIDIA Build, Groq, Gemini AI Studio (incl. Hydrogen), OpenRouter (free Ling-3.2-flash 1M), Cloudflare. AMD MI300X credits.

See [CURRENT.md](CURRENT.md) for the full snapshot.
