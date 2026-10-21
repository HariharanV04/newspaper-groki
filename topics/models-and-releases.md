# Models & Releases

Living document. New entries go at the top. Older entries are refined or marked superseded rather than duplicated.

**Last refined:** 2026-10-21

---

## Frontier / Flagship & Large Open

### DeepSeek DeepInfer + V4.1-Flash (Open-source inference Oct 20; model Oct 17)
- **Type:** Production inference stack (DeepInfer, Apache 2.0) for DeepSeek-V4.1-Flash (multimodal MoE, 1M context, MIT weights). Also deepseek-recipe (MIT).
- **Role:** High-throughput, low-latency serving of agent/coding Flash model. Dual NVIDIA SM100 / Huawei Ascend 950. Significant efficiency claims (cache hit, tok/s).
- **Status:** Framework on GitHub; offline focus (some production pieces held back). Model weights/API live. Strong ongoing relevance.

### Mistral Voxtral 3 (Oct 20, 2026)
- **Type:** Speech family: transcription (50+ langs, diarization; Mini 4B), TTS (35+ langs/dialects), LiveKit voice agent SDK.
- **Role:** Real-time voice agents (listen-reason-speak-tools). Low pricing for transcription.
- **Status:** API available (EU/US/global); self-host on request. Competitive vendor speech benchmarks.

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
- **Type:** Multimodal MoE, 1M context. MIT open weights. Now paired with open DeepInfer.
- **Role:** Reasoning, coding, agentic tasks, vision.
- **Status:** API live. Weights on HF. Continues strong relevance.

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

### Other recent
- **FLUX 3 Image Klein**, **StepFun Step 5 Preview**, **Ling-3.1-flash**, **IBM Granite Switch 4.1**, **LFM2.5-24B-A2B**, **MiniCPM-V 4.7** continue as notable.

## Other / Infrastructure

- DeepInfer open inference framework
- Transformers: Beam, Muse Spark Open, EmbeddingGemma 2, Nemotron diarization, TorchNeuron support, etc.
- TRL fused LM head for efficient post-training
- Diffusers Qwen-Image 2.1
- vLLM TorchTPU, TorchNeuron for non-NVIDIA accelerators

---

*When a model is superseded or major details change, update the existing entry rather than adding a duplicate.*
