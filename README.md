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

## Latest highlights (as of 2026-11-04)

- **Mistral Large 4 (Le Chonk)** — Open weights (1T / ~52B active multimodal MoE) leading open agentic coding with efficiency gains; trained in Europe; high HF traction. TRL supports single-node LoRA fine-tuning.
- **HF Benchmarks** — Daily official updates show shifts; DeepSeek-V4.1-Flash, InternLM previews, and specialized agents (Seshat) claiming new #1s on key boards.
- **Trending HF** — LFM3-1.7B (local agents), Nemotron Transcribe, DeepSeek Flash, Mistral Large 4, Idol, LTX-2.5.
- **P-H3-Image** — PrunaAI open smaller/faster image model from MiniMax-H3.
- **Free APIs** — Verified free tiers on Google AI Studio (Gemini Flash family), Groq, NVIDIA NIM (many models), OpenRouter free models, Cloudflare.
- **Ongoing** — Weight-space programming, Hydrogen-1.0 scientific MoE, LongCat-2.5, local MoE serving (FreeToken), decision models (Drex Max).

See [CURRENT.md](CURRENT.md) for the full snapshot.
