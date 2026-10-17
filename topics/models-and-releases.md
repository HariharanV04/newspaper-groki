# Models & Releases

Living document. New entries go at the top. Older entries are refined or marked superseded rather than duplicated.

**Last refined:** 2026-10-17

---

## Frontier / Flagship & Large Open

### NVIDIA Nemotron 3.5 Super VL & Bolt (Oct 16, 2026)
- **Type:** Open VL (120B total / 12B active) + smaller Bolt MoEs (74B-A9B, E4B)
- **Role:** Fast-track completion for always-on agents; vision/documents/video; open weights + data + recipes
- **Status:** Fresh open release reinforcing NVIDIA open strategy. On Hugging Face.

### Reflection AI Beam (Oct 16-17, 2026)
- **Type:** 501B sparse expert MoE, 1M context, token-efficient
- **Role:** Frontier coding and agentic use cases; open weights
- **Status:** Transformers support (v5.20.1); HF blog + livestream. Infrastructure readiness is the key challenge.

### Meta Muse Spark Open (Oct 15, 2026)
- **Type:** 816B total / 42B active, 1M context, multimodal in → text
- **Status:** Claimed most capable US open-weight. High VRAM; weights on HF.

### Gemini 4 Argon (Google) — GA Oct 13, 2026
- **Role:** Long-horizon frontier model (coding, enterprise knowledge work, cyber defense)
- **Context:** 1M tokens (input + output)
- **Modality:** Native multimodal (text, image, audio, video)
- **Access:** Gemini API (`gemini-4-argon`), AI Studio, Gemini platform, AI Ultra/Pro, Antigravity
- **Pricing:** Intro (to Nov 30) $2 / $10 per 1M tokens; then $4 / $20. Cached input heavily discounted.
- **Status:** Active frontier reference.

### Muse Wonder / Muse Wonder Full (Meta) — Oct 12, 2026
- **Role:** First Meta frontier-class models for personal & professional agents
- **Features:** Active Memory, Active Focus
- **Context:** 1M tokens; multimodal input → text output
- **Access:** Meta Model API + Muse Code
- **Status:** Proprietary. Competitive on agent/memory benchmarks.

## Open-Weight & Efficient Models

### LFM2.5-24B-A2B (Liquid AI) — Oct 13, 2026
- **Type:** MoE, 24B total / ~2B active, reasoning-only
- **Strengths:** On-device agents, tool use, 131K context
- **Status:** Still primary open on-device agent candidate; trending.

### MiniCPM-V 4.7 (OpenBMB)
- **Type:** MoE multimodal (35B-A3B + 1B). Apache 2.0
- **Strengths:** Strong on-device VLM performance
- **Status:** Leading open on-device MoE VLM; DSpark heads available.

### Lumma-Fev-27B & Decision Models (FrontiersMind, AutoTrust JEV/GEV)
- **Type:** Explicit choice + probability outputs
- **Status:** Surging theme for reliable automated workflows.

### Qwen-Image-2.1-Turbo & variants
- **Type:** Accelerated 7B image gen/edit
- **Status:** Highly trending; uncensored/quantized versions popular.

### DeepSeek-V4.1-Flash
- **Status:** Continued strong riser for reasoning and coding.

## Other / Infrastructure

- EmbeddingGemma 2: cross-modal embeddings
- Transformers v5.20.1: Beam + torch fixes
- TRL fused LM head for much longer sequences
- NVIDIA Run:ai open-sourced
- Tencent Agent Memory

---

*When a model is superseded or major details change, update the existing entry rather than adding a duplicate.*
