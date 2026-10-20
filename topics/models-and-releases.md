# Models & Releases

Living document. New entries go at the top. Older entries are refined or marked superseded rather than duplicated.

**Last refined:** 2026-10-20

---

## Frontier / Flagship & Large Open

### MiniMax M3.1 Flash (Oct 19, 2026)
- **Type:** Efficient Flash model for agents/coding/Computer Use. 1M context, multimodal input. Weights forthcoming (Oct 23).
- **Role:** Strong agentic/coding performance at low cost ($0.15/$0.60 per 1M). ~3x faster, 70% lower agent cost vs prior.
- **Status:** API live. Former stealth Space Bunny. Independent notes on high hallucination rate.

### inclusionAI Ming-3.0 Speech Family (Oct 19, 2026)
- **Type:** MIT open audio models: 126B/6.5B MoE audio-flash + tiny variants for understanding/TTS/ASR.
- **Role:** Native audio interaction, dialects, long-form, tool use, paralinguistics.
- **Status:** Weights on HF/ModelScope; day-0 serving support (SGLang/vLLM).

### Meta Muse Glimmer (report Oct 19; model earlier)
- **Type:** 30B dense Apache 2.0, multimodal (text+image), 4-bit friendly for single consumer GPU.
- **Role:** On-device agentic tasks, tool use, multi-step planning. Strong for size class.
- **Status:** Technical report published; practical local deployment emphasized.

### DeepSeek V4.1-Flash-1017 (Oct 17, 2026)
- **Type:** Multimodal MoE (~552B backbone + 196B Engram; 8B active prefill / 16B decode), 1M context. MIT open weights.
- **Role:** Reasoning, coding, agentic tasks, vision. Minor update with broad benchmark gains + faster/shorter outputs.
- **Status:** API live (deepseek-flash). Weights on HF. Continues strong relevance.

### Reflection AI Beam 1.0 (Oct 16, 2026)
- **Type:** 501B total / ~23B active sparse MoE, 1M context, Apache 2.0.
- **Role:** Coding, reasoning, tool use, long-horizon agents. Token-efficient.
- **Status:** Full open weights available. Transformers support.

### Meta Muse Spark Open (Oct 15, 2026)
- **Type:** 816B total / 42B active, 1M context, multimodal in → text.
- **Status:** Open weights (Muse Model License). High VRAM; SGLang/vLLM optimized.

### NVIDIA Nemotron 3.5 Super VL & Bolt (Oct 15, 2026)
- **Type:** Open VL (120B/12B) + Bolt MoEs (74B-A9B for 24GB).
- **Role:** Long-running agents, vision/docs/video. Fully open weights + data + recipes.
- **Status:** Active on HF and NIM.

## Open-Weight & Efficient Models

### Other recent (Oct 15-17)
- **FLUX 3 Image Klein**, **StepFun Step 5 Preview**, **Ling-3.1-flash**, **IBM Granite Switch 4.1** continue as notable.

### LFM2.5-24B-A2B (Liquid AI)
- **Type:** MoE 24B / ~2B active for local agents.
- **Status:** Efficient on-device option.

### MiniCPM-V 4.7 (OpenBMB)
- **Type:** MoE multimodal. Strong on-device VLM.
- **Status:** Trending.

## Other / Infrastructure

- Transformers: Beam, Muse Spark Open, EmbeddingGemma 2, Nemotron diarization, etc.
- TRL fused LM head for efficient post-training
- Diffusers Qwen-Image 2.1

---

*When a model is superseded or major details change, update the existing entry rather than adding a duplicate.*
