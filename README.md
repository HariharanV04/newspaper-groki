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

## Latest highlights (as of 2026-11-20)

- **Google Gemini 4 Neon** — Mid-tier ($3/$15, 1M context, multimodal). Strong on coding agents (#1 AA Coding Agent Index), intelligence (~61), lower cost-per-task than Carbon; live in API, Antigravity, Gemini app, Copilot.
- **RadixArk DaisyRose-27B** — Open Apache RL-tuned Qwen3.8-27B; Terminal-Bench 4.1 5.6%→12.0% from 1,200 tasks in 18 days.
- **Reson8 Rumble-2-Flash** — Open 0.5B multilingual ASR (40+ langs) matching larger models, native Transformers/vLLM.
- **Tencent Hy4 flash open weights** — 220B+ MoE / 12B active multimodal 1M on HF; heavily trending.
- **OVHcloud Olala mini**, **Microsoft Aion**, **Phancy Phai-A1**, Apple FastFrames-L, MiniMax-H3-Image continuing.
- **Trending HF** — Haru-4B (audio), Hy4-flash, FastFrames-L, Qwen pi-adapted (agent), LTX-2.5, MiniMax-H3-Image.
- **Free APIs / GPUs** — Kaggle (~30h/week), Modal ($30/mo), E2B ($100), HF ZeroGPU, Colab, Lightning, NVIDIA NIM, Groq, Gemini AI Studio, OpenRouter, Cloudflare. New student credits + startup programs.

See [CURRENT.md](CURRENT.md) for the full snapshot.
