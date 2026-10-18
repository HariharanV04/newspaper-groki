# Models & Releases

Living document. New entries go at the top. Older entries are refined or marked superseded rather than duplicated.

**Last refined:** 2026-10-18

---

## Frontier / Flagship & Large Open

### DeepSeek V4.1-Flash-1017 (Oct 17, 2026)
- **Type:** Multimodal MoE (~552B backbone + 196B Engram; 8B active prefill / 16B decode), 1M context. MIT open weights.
- **Role:** Reasoning, coding, agentic tasks, vision. Minor update with broad benchmark gains (esp. Terminal-Bench, DeepSWE, ProgramBench) + faster/shorter outputs.
- **Status:** API live (deepseek-flash, unchanged pricing). Trending #1 on Hugging Face. Weights + code on HF. Optimized for DeepSeek Harness v0.2.1+.

### Reflection AI Beam 1.0 (Oct 16, 2026)
- **Type:** 501B total / ~23B active sparse MoE, 1M context, Apache 2.0.
- **Role:** Coding, reasoning, tool use, long-horizon agents. Token-efficient.
- **Status:** Full open weights available. Transformers support. HF blog coverage.

### Meta Muse Spark Open (Oct 15, 2026)
- **Type:** 816B total / 42B active, 1M context, multimodal in → text.
- **Status:** Open weights (Muse Model License). Claimed most capable US open-weight. High VRAM; optimized for SGLang/vLLM. Still trending.

### NVIDIA Nemotron 3.5 Super VL & Bolt (Oct 15, 2026)
- **Type:** Open VL (120B/12B) + Bolt MoEs (74B-A9B for 24GB).
- **Role:** Long-running agents, vision/docs/video. Fully open weights + data + recipes.
- **Status:** Active on HF and NIM.

### Gemini 4 Argon (Google) — GA Oct 13, 2026
- **Role:** Long-horizon frontier (coding, enterprise, cyber).
- **Context / Modality:** 1M, native multimodal.
- **Status:** Active proprietary reference. Pricing $2/$10 intro then higher.

### Muse Wonder / Muse Wonder Full (Meta) — Oct 12, 2026
- **Role:** Proprietary frontier agents with Active Memory/Focus.
- **Status:** Proprietary via Meta Model API.

## Open-Weight & Efficient Models

### Other Oct 15-17 releases
- **FLUX 3 Image Klein** (Black Forest Labs): ~5.6B open image gen/edit.
- **StepFun Step 5 Preview**: 600B / 27B active, 1M context agent model (open weights).
- **Ling-3.1-flash** (InclusionAI): 560B / 25B active, MIT, 1M.
- **IBM Granite Switch 4.1**: Unified chat + decision + speech.

### LFM2.5-24B-A2B (Liquid AI) — Oct 13, 2026
- **Type:** MoE 24B / ~2B active for local agents.
- **Status:** Still trending / primary efficient on-device option.

### MiniCPM-V 4.7 (OpenBMB)
- **Type:** MoE multimodal. Strong on-device VLM.
- **Status:** Trending; Apache 2.0.

### DeepSeek-V4.1-Flash (prior)
- **Status:** Superseded by 1017 checkpoint for API and weights.

### Decision models, Qwen-Image-2.1-Turbo, EmbeddingGemma 2
- Continue as supporting themes (explicit decisions, image gen, cross-modal embeddings).

## Other / Infrastructure

- Transformers ongoing model additions (Beam, Muse Spark, etc.)
- TRL fused LM head improvements still relevant for training

---

*When a model is superseded or major details change, update the existing entry rather than adding a duplicate.*
