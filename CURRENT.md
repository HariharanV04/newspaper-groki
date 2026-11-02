# Current AI Briefing

**Last updated:** 2026-11-02

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24h (Nov 1-2)
- **DeepSeek dsh-superagent v0.1.0**: Open-sourced under MIT as a research-prototype coding agent. Packaged as a DeepSeek Harness bundle. Runs on the user's own machine (Node.js, git, etc.). Watches one GitHub repository (and optionally Feishu). Turns allowed user requests into work items (Tickets) and executes them in isolated worker sessions. Proactive work defaults to observe mode. Router-worker architecture for parallel handling.
- **Nace AI Drex Max v1 27B Decision Model**: Open-sourced under Nace.AI Open RAIL-M. Dense 27B model for decisions instead of generation: one forward pass returns probabilities over supplied options (text or multimodal with screenshots). Includes BF16 weights, Q8_0 GGUF, 4-bit builds, and forks of llama.cpp/Ollama. Runs locally on NVIDIA GPUs (~26GB 8-bit), Apple Silicon (24GB+ for Q4), and CPU. Strong on decision benchmarks (e.g., ~64-67 on Artificial Analysis Decision Index). Ideal for routing, classification, and computer-use agent loops at low latency/cost.
- **Microsoft Mage-VL-Cowork 4B**: Hybrid computer-use vision-language model (4B params). Open release for agentic computer use.
- **SenseTime SenseNova Loop-9B-Preview**: 9B-parameter multimodal model claimed to match 27B-class performance on selected benchmarks. Open-sourced.
- **Baseten (Base Labs) joey-1**: 2B decision model post-trained from Qwen3.5-2B. Returns labels with calibrated probabilities. MIT-licensed weights on Hugging Face. Very low cost on Baseten API ($0.01/1M input tokens).
- **NVIDIA DeepSeek Flash NVFP4 optimization**: Reduced download size of DeepSeek-V4.1-Flash by ~75 GiB via NVFP4 quantization targeting Blackwell GPUs. Modest benchmark shifts; requires modified vLLM.
- **JetBrains Mellum2.1-12B-A2.5B-Thinking-MTP**: Added multi-token prediction (MTP) head for 1.4–1.8× faster decoding with high acceptance rates. Supported in vLLM, transformers, llama.cpp.
- **Alleged Anthropic Mythos-class model leak**: Reported on Hugging Face (large size claims); authenticity and malware concerns raised in community.

### Ongoing traction & recent
- **Mistral Large 4 (ML4 / “Le Chonk”)**: Trillion-parameter open-weight MoE continues strong HF traction. Efficiency claims and coding/cyber performance hold; TRL LoRA support available.
- **DeepSeek-V4.1-Flash-1017** and variants: High downloads and trending for efficient multimodal/image-text-to-text. Free API endpoints available via NVIDIA NIM and others.
- **Liquid AI LFM3 family** (esp. LFM3-1.7B / VL): Strong local/edge performance and HF activity. WebGPU demos noted.
- **Qwen3.8-27B**: Extremely high cumulative downloads (millions) as a capable multimodal model.
- **Pika H3 Flex**: Open-weight ~33B video + synchronized audio model (6-step generation) continues relevance for creative pipelines.
- **baidu/Unlimited-OCR-2** and other document intelligence models active.
- **NVIDIA Nemotron series** (Transcribe, Super VL, Lightning, etc.): Strong free endpoints and open weights for speech, VL, and reasoning.

## Hugging Face & Ecosystem Updates
- **24h / Trending (as of Nov 2)**: deepseek-ai/DeepSeek-V4.1-Flash-1017 (high likes/downloads), LiquidAI/LFM3-1.7B, nvidia/NVIDIA-Nemotron-3.5-Transcribe-30B-A4B, mistralai/Mistral-Large-4-1T-A52B, baidu/Unlimited-OCR-2, Qwen/Qwen3.8-27B (dominant downloads), Lightricks/LTX-2.5 (image-to-video leader), Nanbeige4.3-33B, and GGUF quant variants for local inference.
- Diffusers 0.42+ integrations (FLUX.3 Image Klein, Fibo, Kandinsky, etc.) with Python 3.11+ requirement.
- Community: Decision models (Drex Max, joey-1), coding agents (dsh-superagent), MTP heads, refusal-ablated variants, realtime editing Spaces (Qwen-Image), Phonon TTS browser demos.
- Ecosystem support: Transformers, vLLM, SGLang, TRL, llama.cpp, Ollama, FreeToken for new open weights and MoEs.

## Research (recent arXiv / HF Papers ~Nov 1-2 focus)
- Agent frameworks and evaluation: Co-Design Bench (multimodal collaborative coding with real user requests and acceptance criteria); WeVisCut (script-to-video agent with tool+policy learning, high efficiency).
- Efficiency and inference: LEAP (length prediction for scheduling), GAAC lossless KV compression for personal devices, FreeToken edge-native MoE serving (CPU+GPU+RAM pooling for large models on consumer hardware).
- Safety and agents: Continued work on misalignment, agent reliability, self-improvement (RSI Arena, A-RSI), long-horizon optimization (Multiscale Policy Optimization).
- Scientific and specialized: Ongoing demos of autonomous lab agents (prior gene therapy mouse injection remains notable); papers on ontology engineering, power electronics schematic synthesis, defect detection.
- Themes: Agentic systems for coding/video/editing, local inference efficiency for MoEs, evaluation of multimodal agents, safety probes.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (verified ~Nov 1-2 2026):**
- Google AI Studio / Gemini API: Free tier on Gemini 3.8/3.6/3.5 Flash variants, Gemma 4, etc. (may train on prompts).
- Groq: Free plan with rate limits for gpt-oss, Qwen3.8-27B, etc.
- NVIDIA NIM (build.nvidia.com): Free endpoints for many open models including Nemotron variants, DeepSeek-V4.1-Flash, GLM, Muse, Gemma, etc. (NVIDIA Developer Program key).
- OpenRouter free models: Rotating :free variants (Nemotron, Gemma, Inkling, etc.); limited daily requests.
- Cloudflare Workers AI, Requesty, AIHubMix, and other aggregators with card-free free tiers.
- Hugging Face ZeroGPU, Google Colab, Kaggle for interactive work.
- Local: FreeToken (Apache-2.0) for running large MoE (DeepSeek Flash, Qwen, GLM) on gaming PCs by pooling GPU+CPU+RAM; Ollama, llama.cpp, MLX, vLLM.

**Hosting & tools:**
- DeepSeek Harness + dsh-superagent for local coding agents.
- Decision models (Drex Max, joey-1) for efficient agent routing/computer-use.
- Coding agents with free tiers: GitHub Copilot Free, opencode, Kilo Code, etc. supporting various free models.
- Quantized GGUFs and specialized runtimes for consumer hardware.
- Diffusers/ComfyUI for generation models (Pika H3 Flex, LTX-2.5, FLUX).

## Trending Themes
- Open-weight decision models and specialized small agents (Drex Max, joey-1) for low-latency computer-use and routing loops.
- Local-first coding agents (dsh-superagent) and edge MoE serving (FreeToken) reducing reliance on cloud for large models.
- Continued HF dominance of efficient multimodal open weights (DeepSeek Flash, Qwen, LFM3, Nemotron) with free API access.
- Video and creative generation pipelines (Pika H3 Flex, LTX-2.5) with open weights.
- Agent evaluation and efficiency research (coding benches, length prediction, KV compression).
- Free compute tiers and aggregators making frontier open models widely accessible for developers.
- Dual-use considerations around open coding/decision models and alleged leaks.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor changelogs, arXiv, GitHub). Vendor scores are not independent. Caution on unauthenticated leaks.*
