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

## Latest highlights (as of 2026-11-06)

- **OpenAI GPT-6 Cyber** — Specialized model for authorized vulnerability research. 48.5% on ExploitGym, discovered 81 high-severity Firefox bugs and 948 Linux kernel exploits. Restricted to Daybreak Red; rated Critical.
- **Kimi K3.1 Pro** — Open weights dominating HF (2.8T / 104B active multimodal MoE, 1M context). Tops Agent Arena among open models; near-frontier agentic coding.
- **Gemini Omni 1.2 Flash** — Longer video clips (15s), 30% cheaper.
- **Ripple-65B Preview** — Dense 65B Apache 2.0 model from RicursiveAI; self-reported US open-weight SOTA on Terminal-Bench 2.1.
- **Trending HF** — Kimi K3.1 Pro leading, LTX-2.5, Nemotron Transcribe, Mistral Large 4.
- **Free APIs** — Stable free tiers on Gemini AI Studio (incl. Omni), Groq, NVIDIA NIM, Colab, HF ZeroGPU, OpenRouter, Modal credits.
- **Ongoing** — Mistral Large 4 efficiency leadership, llama.cpp FP8, Together inference compiler, agent research on routing, memory, and long-horizon reliability. Cline and other open coding agents popular.

See [CURRENT.md](CURRENT.md) for the full snapshot.
