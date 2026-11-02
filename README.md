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

## Latest highlights (as of 2026-11-02)

- **DeepSeek dsh-superagent** — MIT open-source research coding agent (router-worker) that runs locally via DeepSeek Harness and manages GitHub repo work items
- **Nace AI Drex Max v1** — 27B open-weight decision model (Open RAIL-M) for local probability-based decisions on Apple Silicon/NVIDIA; ideal for agent loops
- **Local MoE serving** — FreeToken continues enabling large open MoEs (DeepSeek Flash etc.) on consumer GPU+CPU+RAM hardware
- **HF trending** — DeepSeek-V4.1-Flash-1017, LFM3-1.7B, Nemotron Transcribe, Mistral Large 4, Qwen3.8-27B (millions of downloads), LTX-2.5
- **Free APIs** — Verified free tiers on Google AI Studio (Gemini Flash family), Groq, NVIDIA NIM (many models), OpenRouter free models
- **Other releases** — Microsoft Mage-VL-Cowork 4B, SenseTime SenseNova Loop-9B, Baseten joey-1 decision model, NVIDIA NVFP4 size cut for DeepSeek Flash
- **Ongoing** — Mistral Large 4 traction, scientific agent demos (gene therapy mouse, ForTy, PlanAssist), alignment research (Anthropic benign datasets)

See [CURRENT.md](CURRENT.md) for the full snapshot.
