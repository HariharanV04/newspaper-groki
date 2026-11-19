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

## Latest highlights (as of 2026-11-19)

- **Google Gemini 4 Neon** — Mid-tier ($3/$15, 1M context, multimodal). Frontier-level for coding/knowledge/science; faster claims; live in API, Studio, Antigravity, Copilot.
- **Microsoft MAI models** — Code 2 / Flash / Cyber 2 Flash etc. at Ignite: strong price-performance claims; available in GitHub Copilot.
- **OpenAI GPT-6.2 Astra & Sol** — Cheaper successors (1.05M context); in ChatGPT, Codex, API, Copilot.
- **Tencent Hy4 flash open weights** — 220B+ MoE / 12B active multimodal 1M on HF.
- **SenseNova-Loop-9B** — Open ~9B looped multimodal (Apache), competitive with 27B-class, low VRAM.
- **Rumble-2-Flash** — Open 0.5B multilingual ASR matching larger models.
- **Trending HF** — Haru-4B (audio), Qwen pi-adapted (agent), LTX-2.5, Inkling-2-Small, MiniMax-H3-Image, Hy4-flash.
- **Free APIs / GPUs** — Kaggle (~30h/week), Modal ($30/mo), E2B ($100), HF ZeroGPU, Colab, Lightning, NVIDIA NIM, Groq, Gemini AI Studio, OpenRouter, Cloudflare. AMD and startup credits.

See [CURRENT.md](CURRENT.md) for the full snapshot.
