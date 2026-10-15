# Current AI Briefing

**Last updated:** 2026-10-15

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier Model Releases

### Google Gemini 4 Argon (General Availability – Oct 13, 2026)
- Google's new frontier model optimized for long-horizon, multi-step work in software engineering, enterprise knowledge (legal/finance), and cybersecurity defense.
- **Key specs:** Unified 1M-token input+output context window (industry-leading output limit), natively multimodal (text, images, audio, video), tunable thinking levels.
- **Availability:** Gemini API (model ID: `gemini-4-argon`) in AI Studio and Gemini platform; Google AI Ultra/Pro subscribers in Gemini app and AI Mode in Search; Antigravity for Ultra users.
- **Pricing (introductory through Nov 30, 2026):** $2 / 1M input tokens, $10 / 1M output tokens; cached input at 95% off ($0.10). Standard after that: $4 / $20.
- Strong performance on agentic coding (DeepSWE, Vibe Code Bench), knowledge work, and safety (low prompt injection success).

### Meta Muse Wonder & Muse Wonder Full (Released Oct 12, 2026)
- Meta Superintelligence Labs' first frontier-class models, focused on personal and professional agentic tasks (coding, legal/finance/health workflows, long-running agents).
- **Features:** Active Memory (cross-conversation context retention) and Active Focus (goal persistence, error recovery, alternative approaches).
- **Specs:** 1M-token context; multimodal input (text, images, video, audio, PDFs); text output only. Trained at Prometheus data center.
- **Availability:** Muse Wonder via Meta Model API and Muse Code; Muse Wonder Full limited to Muse Code subscribers. Proprietary (no open weights). Will power the Muse personal agent.
- **Pricing (Wonder API):** ~$4 / 1M input, $20 / 1M output; cached $0.20.
- Competitive with Claude Opus 5.5 / Fable 5.1 and GPT-6 Astra on Artificial Analysis Intelligence Index and agent benchmarks. Strong on MemoryBench.

### Other Notable Releases (Oct 12–15)
- **Liquid AI LFM2.5-24B-A2B** (Oct 13): Open-weight MoE (24B total / ~2B active). Reasoning-only model optimized for on-device agents and tool use. 131K context, strong agentic/tool benchmarks. Fast edge inference (~184 tok/s on Apple M5 Max). On Hugging Face.
- **OpenBMB MiniCPM-V 4.7** (Oct 12, with Oct 15 updates): First MoE multimodal in the MiniCPM-V series (35B-A3B + 1B dense). Claims new performance-efficiency Pareto frontier. 35B-A3B runs smoothly on-device (13+ tok/s in ~3 GB on iPhone 17 Pro Max) via Lookahead Expert Scheduling (LES). DSpark speculative decoding heads released Oct 15 (BF16 + GGUF). Apache 2.0. Strong on MMBench, MMMU, OCRBench, OmniDocBench.
- **FrontiersMind Lumma-Fev-27B** (Oct 14): 27B-parameter decision model. Returns explicit choices and calibrated probabilities instead of generated labels/text. Designed for automated workflows; evaluate calibration, task fit, multilingual limits, and cost. Blog + model on Hugging Face.
- **Grok Voice 3.0** (xAI, Oct 14): New voice model topping speech-to-speech indices in early reports (~$0.08/min).
- **Ultramarine 1 Flash** (Paper Instruments, Oct 14).
- **Fish Audio Drama 3**: TTS with script-directed voices; downloadable weights (commercial limits apply).
- **Qwen-Image-2.1-Turbo**: Accelerated 7B checkpoint for text-to-image generation and editing in 8 denoising steps. Open weights; Diffusers / ComfyUI ready. Still highly trending.
- **TencentDB Agent Memory** (v2.0.3-beta.1): MIT-licensed persistent memory for agents (local SQLite + team memory hub).
- NVIDIA open-sourced **Run:ai** (Kubernetes GPU orchestration).

## Hugging Face & Ecosystem
- Decision models surging: Lumma-Fev-27B, AutoTrust JEV-27B-VL / GEV-26B-Decide (previously top trending), and related System 1/System 2 decision heads.
- MiniCPM-V 4.7 35B-A3B and related quantizations gaining traction.
- LFM2.5-24B-A2B and DeepSeek-V4.1-Flash remain strong risers.
- **HF tooling:** Tensor viewer for large sharded models sped up dramatically (fetches all shard headers in one request; e.g. DeepSeek-V3.2 loads in 0.45s vs 9.2s).
- Transformers v5.19: EmbeddingGemma 2 (cross-modal embeddings), Nemotron 3 Diarization.
- Diffusers 0.41: Qwen-Image 2.1 support.
- Ongoing high volume of quantizations, LoRAs, decision models, and robotics checkpoints.

## Research
- **Lumma-Fev-27B** evaluation blueprint (calibration, task fit, multilingual limits).
- **VKORE-46M-NPU**: Backpropagation / full training loop demonstrated on an inference-first NPU.
- **ColGrep-Agent-2B**: Local search agent that reduces context tax for coding assistants.
- NVIDIA practical evaluation blueprint for domain-specific speech recognition (air-traffic-control study).
- **HiRO-ACEv2**: Extreme weather simulation at 3 km resolution at fraction of prior cost (AllenAI).
- Continued: QwenGyre (xLong agent RL), robotics distillation speedups, agent memory, multimodal embeddings, on-device efficiency.

## Free GPUs, Hosting & Tools
**Free / low-cost compute:**
- Google Colab free tier (limited T4, ~12h sessions)
- Kaggle Notebooks (T4 ×2, ~30h/week)
- Hugging Face ZeroGPU (shared high-end for Gradio Spaces; short daily quota)
- Lightning AI free plan (persistent studios, monthly GPU hours)
- NVIDIA Developer free endpoints (build.nvidia.com) — many large open-weight models via OpenAI-compatible API
- Modal / Replicate free credits; Oracle Always Free (CPU); RunPod / Vast.ai spots

**Hosting & tooling:**
- Hugging Face Spaces + Hub
- vLLM, SGLang, llama.cpp, TensorRT-LLM
- Diffusers + ComfyUI for image pipelines
- Tencent Agent Memory and other agent memory / MCP stacks
- NVIDIA Run:ai for cluster GPU governance
- Free LLM API directories (updated Oct 14) listing 100+ models across 30+ providers with verified free tiers

## Trending Themes
- Decision models (explicit choices + probabilities instead of free generation)
- Agentic workflows (long-running tasks, memory, focus/recovery, on-device agents)
- Efficiency via low-active-parameter MoEs and accelerated diffusion
- Open-weight vs proprietary frontier models
- Multimodal embeddings, robotics real-time inference, cybersecurity applications
- On-device / edge multimodal (especially MoE VLMs)

---
*Always verify latest benchmarks, pricing, and availability on official sources.*