# Models & Releases

Living document. New entries go at the top. Older entries are refined or marked superseded rather than duplicated.

**Last refined:** 2026-10-15

---

## Frontier / Flagship

### Gemini 4 Argon (Google) — GA Oct 13, 2026
- **Role:** Long-horizon frontier model (coding, enterprise knowledge work, cyber defense)
- **Context:** 1M tokens (input + output)
- **Modality:** Native multimodal (text, image, audio, video)
- **Access:** Gemini API (`gemini-4-argon`), AI Studio, Gemini platform, AI Ultra/Pro, Antigravity
- **Pricing:** Intro (to Nov 30) $2 / $10 per 1M tokens; then $4 / $20. Cached input heavily discounted.
- **Status:** Active frontier reference. Watch for subsequent Gemini 4 variants.

### Muse Wonder / Muse Wonder Full (Meta) — Oct 12, 2026
- **Role:** First Meta frontier-class models for personal & professional agents
- **Features:** Active Memory, Active Focus
- **Context:** 1M tokens; multimodal input → text output
- **Access:** Meta Model API + Muse Code (Wonder); Wonder Full restricted to Muse Code subscribers
- **Pricing (Wonder API):** ~$4 / $20 per 1M tokens
- **Status:** Proprietary. Competitive on agent/memory benchmarks. Powers Muse personal agent.

## Open-Weight & Efficient Models

### Lumma-Fev-27B (FrontiersMind) — Oct 14, 2026
- **Type:** 27B decision model (returns choices + probabilities, not free text generation)
- **Strengths:** Explicit decisions for automated workflows; evaluate calibration and task fit before production use
- **Status:** Newly released; blog post on HF highlights practical evaluation considerations

### LFM2.5-24B-A2B (Liquid AI) — Oct 13, 2026
- **Type:** MoE, 24B total / ~2B active, reasoning-only
- **Strengths:** On-device agents, tool use, 131K context, strong agentic benchmarks vs larger models
- **Performance notes:** ~184 tok/s on Apple M5 Max; competitive with larger Qwen MoEs on several agent tasks
- **Status:** Primary open-weight on-device agent candidate this week

### MiniCPM-V 4.7 (OpenBMB) — Oct 12, 2026 (updated Oct 15)
- **Type:** First MoE multimodal in MiniCPM-V series (35B-A3B + 1B dense). Apache 2.0
- **Strengths:** New performance-efficiency Pareto frontier; 35B-A3B runs smoothly on-device (13+ tok/s, ~3 GB on iPhone 17 Pro Max) via LES. Strong multimodal/OCR/document benchmarks
- **Updates:** DSpark speculative decoding heads (BF16 + GGUF) released Oct 15 for both sizes
- **Status:** Leading open on-device MoE VLM

### Qwen-Image-2.1-Turbo (Alibaba Qwen)
- **Type:** 7B accelerated image generation + editing checkpoint
- **Key change:** 8 denoising steps (vs ~40 on base)
- **Status:** Highly trending on Hugging Face; Diffusers + ComfyUI ready

## Other Recent Releases

- **Grok Voice 3.0** (xAI, Oct 14) — voice model topping early speech-to-speech indices
- **Ultramarine 1 Flash** (Paper Instruments, Oct 14)
- **Fish Audio Drama 3** — script-directed TTS with downloadable weights (commercial limits)

## Infrastructure / Supporting Releases

- **TencentDB Agent Memory** v2.0.3-beta.1 (Oct 13) — MIT, local SQLite + team memory hub
- **NVIDIA Run:ai** — fully open-sourced Kubernetes GPU orchestration
- **Transformers v5.19** — EmbeddingGemma 2, Nemotron 3 Diarization
- **Diffusers 0.41** — Qwen-Image 2.1 support
- HF tensor viewer optimization for large sharded models (single-request shard headers)

---

*When a model is superseded or major details change, update the existing entry rather than adding a duplicate.*