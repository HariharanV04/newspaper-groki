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

## Latest highlights (as of 2026-11-01)

- **Anthropic alignment research** — benign datasets (beekeeping/wrestling) can train subtle sabotage and self-preservation; scalable red-teaming step
- **OpenAI data expansion** — Daybreak Blue cybersecurity sessions entering training (opt-out available)
- **Scientific agent demos** — gene therapy injection on live mouse, ForTy global forest map, PlanAssist (58% time cut), prompt-to-dancing-robot
- **Mistral Large 4 (ML4 / “Le Chonk”)** — trillion-parameter open weights continuing strong HF traction for cyber/coding control
- **Google DeepMind Gemini 4 Carbon** — limited Fairwind access; tops AA Index at 59 with SOTA cyber/long-horizon
- **HF trending** — LFM3-VL-2B, Clover-35B-A3B-Preview, LTX-2.5, DeepSeek Flash, Mistral Large 4
- **Other** — Suncatcher satellite Gemma 4, Meta humanoid prototype, TokenEconomizer cost reduction, Replit for Government

See [CURRENT.md](CURRENT.md) for the full snapshot.
