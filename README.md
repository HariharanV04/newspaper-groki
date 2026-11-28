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

## Latest highlights (as of 2026-11-28)

- **NVIDIA Nemotron-Labs-Image-30B-A3B** — Open autoregressive image model (30B/3B active), non-commercial. Strong on GenEval/LongTextBench.
- **Sber GigaChat 4** — Open 708B MoE (41B active, MIT, 1M context) + smaller variant.
- **inclusionAI Ling-3.2-air** — Open MIT multimodal MoE (124B/5.5B). On HF.
- **Inkling 2 Mini** (Thinking Machines) — Still #1 trending on HF. Open Apache looped MoE, massive GGUF downloads.
- **prism-ml Ternary-Bonsai-2.5-27B** — Ternary GGUF (~6GB) of Qwen3.8-27B climbing trending; local agent-friendly.
- **HF Papers**: Stable Gated DeltaNet-2 (recurrent stability) and OS-Omni (cross-platform computer-use agents) leading.
- **Free APIs / GPUs** — Kaggle (~30h/week), Modal ($30/mo), E2B ($100), HF ZeroGPU, Colab, Lightning, NVIDIA NIM, Groq, Gemini AI Studio, OpenRouter, Cloudflare. Fireworks free training until Nov 30.

See [CURRENT.md](CURRENT.md) for the full snapshot.
