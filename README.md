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

## Latest highlights (as of 2026-10-31)

- **Mistral Large 4 (ML4 / “Le Chonk”)** — trillion-parameter (1T/52B active) open weights fully available on HF/API (Oct 29) for cybersecurity and agentic coding; claims ~47% fewer tokens than GLM-5.3 with strong performance; TRL single-node fine-tune example
- **Google DeepMind Gemini 4 Carbon** — next frontier model (Oct 28) with SOTA cybersecurity + long-horizon agents; tops AA Index v5 at 59; limited Fairwind/cyber-defender access; intro $2/$10
- **NVIDIA Nemotron 3.5 Transcribe** — open-weight multilingual ASR with speaker diarization and audio Q&A
- **Ai2 OlmoEarth v1.3** — open satellite embeddings + global 10m precomputed annual data for Earth observation
- **Pika H3 Flex** — open-weight video model with 6-step gen + synchronized multi-stem audio
- **Liquid AI LFM3** — compact open-weight multimodal family for local/edge agents
- **DeepSeek-V4.1-Flash**, **Nanbeige4.3-33B**, **Flint**, **FLUX.3 Image Klein** continue as high-traction open tools

See [CURRENT.md](CURRENT.md) for the full snapshot.
