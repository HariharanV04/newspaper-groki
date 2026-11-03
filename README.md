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

## Latest highlights (as of 2026-11-03)

- **Weight-Space Programming** — MIT CSAIL showed GPT-6 Astra can directly read and edit neural network weights (0.016% of Qwen3.5-0.8B), boosting MATH-500 from 7.9% to 48.1% with no gradients or training.
- **Hydrogen-1.0** — Deep Principle 753B open-weight (MIT) scientific MoE post-trained from GLM-5.3 on lab data; claims edge over GPT-6 Astra on FrontierScience-Research.
- **LongCat-2.5** — Meituan 1.6T native multimodal agentic model (API live, weights coming soon) for long-horizon coding and visual tasks.
- **Mistral Large 4 (Le Chonk)** — Continues strong HF traction as top open coding-agent model with efficiency gains.
- **HF trending** — DeepSeek-V4.1-Flash-1017, Qwen3.8-27B (millions of downloads), LFM3, Nemotron, LTX-2.5, Mistral Large 4.
- **Free APIs** — Verified free tiers on Google AI Studio (Gemini Flash family), Groq, NVIDIA NIM (many models), OpenRouter free models, Cloudflare.
- **Ongoing** — Local MoE serving (FreeToken), decision models (Drex Max), coding agents (dsh-superagent), scientific and agent research.

See [CURRENT.md](CURRENT.md) for the full snapshot.
