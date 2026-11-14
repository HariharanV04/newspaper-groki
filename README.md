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

## Latest highlights (as of 2026-11-14)

- **llama.cpp / ggml v1.0.0** — Stable major release with semantic versioning for the public C API, FP8 KV caches, MoE expert cache, new model support (Kimi-K3.1-Pro, Ripple, etc.), hardened server. Stabilizes local inference after 3.5 years.
- **Gemini 4 Hydrogen** — Google’s fast agentic model (1M context, $1.50/$7.50, xhigh thinking); widely available incl. free tiers, strong speed claims vs prior Flash, competitive with Argon on some indexes.
- **OpenAI Daybreak Red Team + Defense Factory** — AI agent products for web app pen-testing and automated vulnerability patching (early access / preview).
- **MiniMax H3-Image** — Continues top HF trending: native 4K T2I + multi-ref editing, open weights (community license with regional exclusions).
- **Edge0-145B** — Open-weight latent MoE (145B/~10B active) for local/single NVIDIA GPU; high reported speeds and Terminal-Bench; weights on HF (commercial restrictions).
- **PAN 2** — 29B Apache 2.0 world model from IFM/MBZUAI for action-conditioned video simulation; Diffusers support.
- **Trending HF** — Uncensored DeepSeek variants leading, MiniMax-H3-Image, Arete-27B, idol, LTX-2.5, Qwen3.8-27B family, Kimi K3.1 Pro, Ripple-65B.
- **Free APIs / GPUs** — Stable free tiers on Kaggle (~30h/week), Colab, HF ZeroGPU, Lightning/Modal credits, NVIDIA NIM, Groq, Gemini AI Studio (incl. Hydrogen), OpenRouter, Cloudflare. AMD MI300X credits.

See [CURRENT.md](CURRENT.md) for the full snapshot.
