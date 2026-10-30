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

## Latest highlights (as of 2026-10-30)

- **Mistral Large 4 (ML4 / “Le Chonk”)** — trillion-parameter open weights released on HF/API (Oct 29) for cybersecurity and coding; claims 47% fewer tokens than GLM-5.3 with strong agentic coding
- **Pika H3 Flex** — open-weight video model (post-trained MiniMax H3) with 6-step gen, synchronized multi-stem audio, 4K, multi-reference; #1 open on DesignArena t2v
- **Google DeepMind Gemini 4 Carbon** — next frontier model (Oct 28) with SOTA cybersecurity + long-horizon agents; tops AA Index v5 at 59; limited Fairwind access; intro $2/$10
- **Liquid AI LFM3** — open-weight ~2B multimodal family (text/VL/audio/omni/decision) on HF; 256K context, ~1 GB 4-bit, single-GPU fine-tune
- **Google DeepMind Genie 4** — real-time world model with native audio, improved physics/realism, NL steering (research preview)
- **OpenAI GPT-6.1 Terra** — mid-tier computer-use model at half price ($1/$5), stronger agent benchmarks
- **Nanbeige4.3-33B** — open 33B dense Apache 2.0 agentic coding teacher model with 512K context
- **Microsoft Agensh** — open-sourced decentralized harness scaling to 1,024 self-organizing coding agents (MIT)
- **Kimi K3.1 Pro** — near-frontier 2.8T/104B MoE (open weights due Nov 4)
- **Carbon-X, Flint, Nemotron Bolt E4B / Transcribe, MiniMax M3.1 Flash** continue as key open tools

See [CURRENT.md](CURRENT.md) for the full snapshot.
