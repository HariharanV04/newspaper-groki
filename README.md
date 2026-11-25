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

## Latest highlights (as of 2026-11-25)

- **Z.ai GLM-5.4** — First Loop Transformer flagship (~750B scale, 28 layers ×2), 1M context, native multimodal, generalized coding. Hosted; weights after safety. Claims 2T-3T-class intelligence.
- **Baidu ERNIE 5.5 Flash Preview** — Open Apache 280B MoE (14B active), 1M context. Day-0 vLLM. On HF.
- **PrismML Ternary Bonsai 2.5 27B** — Open ternary GGUF (~5.9GB) for long agent runs. SWE gains.
- **Ant Group Ling-3.2-air** — Open MIT multimodal MoE (124B/5.5B). On HF.
- **Inkling 2 Mini** (Thinking Machines / HF) — Open Apache looped MoE (~26B/3B active), multimodal 1M context, ~20GB local-friendly. Still #1 trending; leads open <100B on agent benches.
- **Tencent Hy-MT3 + SenseNova U1.6** — Open translation (102 langs) and self-correcting image models.
- **Claude Ship** — Anthropic agents for automated GitHub PR review, patching, and approvals.
- **Free APIs / GPUs** — Kaggle (~30h/week), Modal ($30/mo), E2B ($100), HF ZeroGPU, Colab, Lightning, NVIDIA NIM, Groq, Gemini AI Studio, OpenRouter, Cloudflare. Shadeform H100 from ~$2.73/hr. Local stacks boosted by Inkling Mini + Ternary Bonsai.

See [CURRENT.md](CURRENT.md) for the full snapshot.
