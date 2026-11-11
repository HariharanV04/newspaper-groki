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

## Latest highlights (as of 2026-11-11)

- **Anthropic Claude Fable 5.2 / Mythos 5.2** — ~30% faster, $8/$40, tops AA Intelligence Index (65). 1,000 agents formalized Fermat in 30h; strong coding/science. Mythos gated for vetted cyber/life-sciences.
- **Google Gemini 4 Carbon GA** — Intro $2/$10 (to Nov 30). Competitive with Fable; AlphaProof Code verified Signal protocol on real machine code.
- **Meta Muse Ember** — Small/cheap multimodal agent model ($0.10/$0.50) for tool calls, routing, extraction.
- **Meituan LongCat-2.5** — Full MIT open weights (1.6T MoE / ~48B active multimodal).
- **Trending HF** — idol (image-to-3D), uncensored DeepSeek, Kimi K3.1 Pro, Ripple-65B, MiniMax-H3-Image, LTX-2.5, Qwen3.8-27B.
- **Free APIs / GPUs** — Stable free tiers on Kaggle (~30h/week), Colab, HF ZeroGPU, Lightning/Modal credits, NVIDIA NIM, Groq, Gemini AI Studio, OpenRouter, Cloudflare. New AMD MI300X credits.
- **Ongoing** — Frontier price war, agent formalization/verification/robotics leaps (GR00T 2), Claude workspace features (Whiteboards/Sheets/Data), open-weight traction (Kimi, Mistral Large 4).

See [CURRENT.md](CURRENT.md) for the full snapshot.
