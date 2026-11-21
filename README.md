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

## Latest highlights (as of 2026-11-21)

- **Inkling 2 Mini** (Thinking Machines / HF) — Open Apache looped MoE (~26B/3B active), multimodal 1M context, ~20GB local-friendly. Leads open <100B on agent benches.
- **Tencent Hy4 full open weights** — 770B/49B active multimodal MoE flagship (1M, vision + computer use) under Tencent Hy License + System Card.
- **Tencent WeMM-Video** — Omni-modal video understanding family (2B–35B-A3B), Apache 2.0, claimed open SOTA.
- **Cloudflare Clairic** — Open 27B + 9B flash for structured schema extraction.
- **alphaXiv Society of AI Scientists** — 936 agents produced 936 papers + own journal in 12 weeks with executable peer review.
- **Free APIs / GPUs** — Kaggle (~30h/week), Modal ($30/mo), E2B ($100), HF ZeroGPU, Colab, Lightning, NVIDIA NIM, Groq, Gemini AI Studio, OpenRouter, Cloudflare. Local stacks boosted by Inkling Mini.

See [CURRENT.md](CURRENT.md) for the full snapshot.
