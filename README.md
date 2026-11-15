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

## Latest highlights (as of 2026-11-15)

- **Unsloth Dynamic V3.1 GGUFs for Qwen3.8-27B** — 5–10% accuracy gains on Terminal Bench, DeepSWE and more vs prior quants; runnable on 12GB RAM. Highest-accuracy local builds for the popular 27B vision model.
- **Weight-space programming** — Lifts Qwen 3.5 0.8B from 7.4% to 58.7% on Math 500 via direct weight edits.
- **Inkling 2 Small weights live** — Thinking Machines 594B/17B MoE under Apache 2.0 on HF with day-0 serving support.
- **MiniMax H3-Image** — Continues top HF trending: native 4K T2I + multi-ref editing, open weights (community license with regional exclusions).
- **Gemini 4 Hydrogen** — Google’s fast agentic model (1M context, $1.50/$7.50, xhigh thinking); widely available incl. free tiers.
- **Trending HF** — MiniMax-H3-Image, uncensored DeepSeek variants, Unsloth Qwen3.8 GGUFs, Inkling-2-Small, Arete-27B, Kimi K3.1 Pro, idol, LTX-2.5.
- **Free APIs / GPUs** — Stable free tiers on Kaggle (~30h/week), Modal ($30/mo), Daytona ($200 signup), HF ZeroGPU, Lightning credits, NVIDIA NIM, Groq, Gemini AI Studio (incl. Hydrogen), OpenRouter (free Ling-3.2-flash 1M), Cloudflare. AMD MI300X credits.

See [CURRENT.md](CURRENT.md) for the full snapshot.
