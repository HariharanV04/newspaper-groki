# Models & Releases

Living document. New entries go at the top. Older entries are refined or marked superseded rather than duplicated.

**Last refined:** 2026-10-28

---

## Frontier / Flagship & Large Open

### Liquid AI LFM3 family (Oct 27, 2026)
- **Type:** Six open-weight ~2B models from shared LFM3-1.7B-Base backbone. Text (1.73B, 256K ctx), VL (video), Audio (speech in/out), Omni, and two decision models (typed outputs). Tri-hybrid architecture.
- **Role:** Local/edge agents, specialized fine-tuning, multimodal on-device. ~1 GB at 4-bit. Single-GPU fine-tune.
- **Status:** Weights + GGUF/MLX/ONNX/FP8 on HF. Liquid reports strong agentic/local performance (self-reported). LFM Open License.

### OpenAI GPT-6.1 Terra (Oct 26, 2026)
- **Type:** Mid-tier closed model (1.05M context) optimized for visual reasoning and computer use.
- **Role:** High-volume everyday agentic work at half prior Terra price ($1/$5). Stronger Terminal-Bench, Agents’ Last Exam, lower errors, faster than higher-end siblings on many tasks (OpenAI figures).
- **Status:** Live in ChatGPT Work, Codex, and API (`gpt-6.1-terra`).

### Google DeepMind Genie 4 (Oct 27, 2026)
- **Type:** Real-time interactive world model with native audio generation.
- **Role:** Photorealistic simulations with real-time NL steering, better physics/humans, up to ~2 min consistency. For robotics training, creative pre-vis, gaming, etc.
- **Status:** Research preview (trusted testers). Expanding to Google AI Ultra (Project Genie) and early Gemini API partners.

### Nanbeige4.3-33B (Oct 24-25, 2026)
- **Type:** 33B dense transformer (Llama-style, 52 layers, GQA), Apache 2.0, 512K context, BF16 (~66GB). English/Chinese.
- **Role:** Flagship teacher for Nanbeige4.3 series; agentic coding and cowork tasks. Self-reported SOTA in ~30B open class on most agent/coding benches (e.g. Terminal-Bench 2.1 80.9, DeepSWE 65.5).
- **Status:** Weights + Base on HF. Transformers/SGLang/vLLM support (TP=4). Thinking default on. Quantizations appearing.

### Microsoft Agensh (open-sourced Oct 24, 2026)
- **Type:** Decentralized multi-agent harness (MIT) for up to 1,024 self-organizing coding agents.
- **Role:** Scales agent organizations without central orchestrator; improves ProgramBench pass rates via concurrent self-assignment, shared Git/messaging/context.
- **Status:** Full code + reproduction guide open. Preprint arXiv:2609.26781.

### Moonshot AI Kimi K3.1 Pro (Oct 23, 2026)
- **Type:** 2.8T total / 104B active MoE, 1M context, multimodal (text+image).
- **Role:** Frontier-class coding, agentic, 3D/CAD, finance. Independent Intelligence Index 55 (4th). Strong Terminal-Bench and other agent scores. Cyber data filtered for open release.
- **Status:** API live ($2/$10). Open weights due Nov 4, 2026. Highspeed variant available. Large hardware needs.

### Hugging Face Carbon-X (Oct 22, 2026)
- **Type:** 14B multimodal (Qwen3-14B base) for DNA sequence analysis/generation + natural language.
- **Role:** Scientific tool for querying genomic effects, mutations, gene activity; local-runnable for privacy.
- **Status:** Open weights released. First-of-kind DNA chat model from HF.

### Recursive Flint (Oct 21-22, 2026)
- **Type:** 40B MoE (~2.5B active), Apache 2.0 coding model.
- **Role:** Local laptop coding agent (high tok/s on consumer hardware). Largely AI-developed via Eureka Machine.
- **Status:** Weights freely available. Strong for on-device/local use.

### MiniMax M3.1 Flash (API Oct 19; weights Oct 23, 2026)
- **Type:** Efficient Flash MoE (428B/23B active), 1M context, multimodal for agents/coding.
- **Role:** Low-cost high-performance agentic/coding ($0.15/$0.60). Day-0 vLLM/NeMo support.
- **Status:** Weights public. Continues strong relevance; note on hallucination tendencies.

### NVIDIA Nemotron 3.5 Bolt E4B 4GB (Oct 23, 2026)
- **Type:** Small open model (~8B/4B effective) post-trained from Gemma 4 E4B.
- **Role:** Local conversational agents, voice, NPCs, embedded. ~4GB VRAM, 64K context, multi-turn tools.
- **Status:** Open weights (BF16 + Q4 GGUF) on HF, Ollama, etc. OpenMDW-1.1.

### DeepSeek DeepInfer + V4.1-Flash (Open-source inference Oct 20; model Oct 17)
- **Type:** Production inference stack (DeepInfer, Apache 2.0) for DeepSeek-V4.1-Flash (multimodal MoE, 1M context, MIT weights).
- **Role:** High-throughput, low-latency serving. Dual NVIDIA / Huawei.
- **Status:** Framework on GitHub; model live. Ongoing relevance.

### Mistral Voxtral 3 (Oct 20, 2026)
- **Type:** Speech family: transcription, TTS, LiveKit voice agent SDK.
- **Role:** Real-time voice agents. Competitive pricing.
- **Status:** API available; self-host on request.

### inclusionAI Ming-3.0 Speech Family (Oct 19, 2026)
- **Type:** MIT open audio models: large MoE + tiny for understanding/TTS/ASR.
- **Role:** Native audio interaction.
- **Status:** Weights on HF; day-0 serving.

### Meta Muse Glimmer
- **Type:** 30B dense Apache 2.0, multimodal, 4-bit friendly.
- **Role:** On-device agentic tasks.
- **Status:** Practical local deployment.

### Reflection AI Beam 1.0 (Oct 16, 2026)
- **Type:** 501B/23B sparse MoE, 1M context, Apache 2.0.
- **Role:** Coding, agents, long-horizon.
- **Status:** Full open weights.

### Meta Muse Spark Open (Oct 15, 2026)
- **Type:** 816B/42B, 1M context, multimodal.
- **Status:** Open weights under custom license.

### NVIDIA Nemotron 3.5 series (Oct 15+)
- **Type:** Super VL 120B + Bolt MoEs for 24GB + now E4B 4GB.
- **Role:** Agents, vision, docs, local conversational.
- **Status:** Fully open; active on HF/NIM. Bolt E4B just released.

## Open-Weight & Efficient Models

### Other recent
- Qwen3.8 variants, DeepSeek Flash updates, Kling 4.0, Canva image model, OlmoEarth, various decision and embedding models continue as notable.
- Block Dessa (speech-to-speech, research preview only).

## Other / Infrastructure

- Kimi K3.1 Pro (open weights pending)
- Carbon-X genomic model
- Flint local coding
- DeepInfer open inference
- Nemotron small models for local agents
- LFM3 family for multimodal edge
- Transformers ongoing support
- TRL, Diffusers updates

---

*When a model is superseded or major details change, update the existing entry rather than adding a duplicate.*
