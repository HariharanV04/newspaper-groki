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

## Latest highlights (as of 2026-10-21)

- **DeepSeek DeepInfer** — production inference framework open-sourced (Apache 2.0) for V4.1-Flash, NVIDIA + Huawei support, high throughput claims
- **Mistral Voxtral 3** — speech transcription/TTS + voice agent SDK (LiveKit), low-cost multilingual
- **HF TorchNeuron** — native PyTorch backend for AWS Trainium (public beta), strong Transformers support
- **MiniMax M3.1 Flash**, **inclusionAI Ming-3.0**, **Meta Muse Glimmer**, DeepSeek-1017, Beam, Muse Spark, Nemotron still key
- Free compute: Colab, Kaggle, ZeroGPU, NVIDIA NIM, Run:ai, etc. stable

See [CURRENT.md](CURRENT.md) for the full snapshot.
