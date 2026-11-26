# Current AI Briefing

**Last updated:** 2026-11-26

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24h (Nov 25-26)
- **Together AI Preemptible Compute** (Nov 24-25): Generally available on GPU Clusters. Same NVIDIA hardware as on-demand at a flat 50% of the rate (no spot bidding). 5-minute drain/SIGTERM for checkpointing; automatic refill. Sub-hourly billing. For interruption-tolerant workloads (training, batch inference, sweeps). Kubernetes and Slurm support across regions.
- **TRL v1.19.0** (Nov 25): Multi-teacher DistillationTrainer (dict of teachers + teacher_id column), environment_factory for stateful distillation. Packed SFT 2x faster with SDPA. AsyncGRPOTrainer out of experimental.
- **Diffusers 0.43.0** & **Transformers updates**: Five new modular pipelines (image gen/editing, video+audio, speech-driven animation). Support for MiniMax-H3-Image, Pika H3 Flex, Inkling 2 Small, MiniCPM-OCR, and more. Python 3.11+ required; trust_remote_code fixes.
- **Inkling 2 Mini** (still heavily trending): Open Apache looped MoE (~26B total / 3B active), multimodal 1M context, local-friendly. #1 trending on HF with massive GGUF downloads (unsloth variants in millions). Leads open <100B on agent benches.
- **Baidu ERNIE 5.5 Flash Preview**: Open Apache 280B MoE (14B active), 1M context. Day-0 SGLang/vLLM. Speculative decoding. Strong agentic scores reported.
- **Ant Group Ling-3.2-air**: Open MIT multimodal MoE (124B/5.5B). On HF; strong AutomationBench gains.
- **PrismML Ternary Bonsai 2.5 27B**: Open ternary GGUF (~5.9GB) for long agent runs. SWE gains.
- **Other ongoing**: Cognition SWE-2.1 (RL on Kimi K3); Tencent Hy-MT3 translation (102 langs); SenseNova U1.6 self-correcting image; NVIDIA Nemotron image models; Sand AI MAGI-2 video; GLM-5.4 Loop Transformer flagship.

### Hugging Face trending (as of Nov 26)
thinkingmachines/Inkling-2-Mini (#1), unsloth/Inkling-2-Mini-GGUF (millions of downloads), inworld/voice-isolator, AtomicChat/Inkling-2-Mini-Uncensored-GGUF, prism-ml/Ternary-Bonsai-2.5-27B-GGUF, inclusionAI/Ling-3.2-air, baidu/ERNIE-5.5-Flash-Preview, Lightricks/LTX-2.5, apple/DepthPro2. Strong activity on looped/efficient local models, MoE, agent adapters, audio isolation, and visual models.

## Hugging Face & Ecosystem Updates
- TRL v1.19.0: Multi-teacher distillation and faster packed SFT.
- Diffusers 0.43.0: New pipelines for MiniMax-H3-Image, Pika H3 Flex, etc. Improved attention, tensor parallelism, LoRA.
- Transformers: Support for Inkling 2 variants, MiniCPM-OCR, and recent multimodal/document models. v5.24.x patches for compatibility.
- HF Blog: Loop-Behind Decoding, robot agents (learned motion + explicit control), multilingual voice agents, decision models for documents, Wonder Agent on-device design.
- Day-0/strong support for new open models (ERNIE, Ling, Bonsai, Inkling, Hy-MT3) across Transformers, vLLM, SGLang, Unsloth, llama.cpp, MLX.
- Local/edge accessibility accelerating with ternary/quantized efficient models and GGUF dominance.

## Research (recent arXiv / HF Papers ~Nov 25-26 focus)
- Lazy Agents Answer Against Their Own Beliefs: RL with verifiable beliefs to reduce premature commitment in long tasks (HF Papers #1).
- Nemotron-Labs-VisualCreation: Agentic framework treating pixels as code for precise visual creation.
- ACAP: Asynchronous Coding Agents for Efficient Robot Control.
- Disclosure Bias in AI Reviewers: Systematic lower scores when AI involvement disclosed (arXiv 2611.30410).
- Ongoing: agent skill learning, long-context efficiency, looped architectures, medical/decision models, formal verification, alphaXiv autonomous agent-generated preprints.
- Broader: Efficiency of looped/MoE, memory systems, agentic science, multimodal robotics.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (as of Nov 26 2026):**
- **Kaggle Notebooks**: ~30 GPU hours/week on 2×T4 (sessions ≤12h). Most reliable free quota for experiments/fine-tuning. Phone verification. No card.
- Google Colab free: T4 when available, session/quota limits.
- Hugging Face ZeroGPU: Short daily shared high-end GPU minutes (5 min free) for Gradio Spaces (PRO much more). Demo-oriented.
- Modal: $30 free credits/month on Starter.
- Lightning AI: Free credits / studios (up to ~50 GPU hours).
- E2B sandboxes: One-time $100 usage credits on Hobby (no card).
- Cloudflare Workers AI, Groq free tier, Google AI Studio, OpenRouter free models, NVIDIA NIM free endpoints, ModelScope, Paperspace Gradient (public projects), Baidu AI Studio.
- **Together AI**: Preemptible compute at 50% of on-demand (same GPUs, interruptible with 5-min drain). Cheap paid options via Shadeform H100 from ~$2.73/hr; RunPod/Lambda competitive.
- Startup/student programs: Thunder Compute $20, Crusoe, Inference.net grants, etc. Fireworks AI free training for select models through Nov 30.
- Local: llama.cpp, Unsloth GGUFs (Inkling, Bonsai ternary, Qwen), MLX. Inkling 2 Mini and Ternary Bonsai practical on consumer hardware.

**Hosting & tools:**
- Open weights gaining: ERNIE 5.5 Flash, Ling-3.2-air, Ternary Bonsai, Hy-MT3, SenseNova U1.6, Inkling Mini.
- Coding/agent tools: Claude Code (still top-ranked for most devs, high merge rates), OpenAI Codex, Cursor, GitHub Copilot, Devin, Google Antigravity, Cline, OpenCode. Cognition SWE-2.1. Anthropic Claude Ship for PR automation.
- Inference: Strong day-0 support (vLLM/SGLang for ERNIE, etc.). Unsloth for local fine-tuning. TRL for distillation/SFT.
- Security tooling: Shirudo (OpenAI+Cisco) for agent eBPF shields continues relevant.

## Trending Themes
- Loop Transformer architectures: GLM-5.4 (large-scale flagship), Inkling 2 Mini (local dominant on HF), others — deeper reasoning via repeated shared-layer passes.
- Efficient open local models: Ternary quantization (Bonsai 5.9GB), looped MoEs, GGUF dominance.
- Open multimodal and specialized: Ling-3.2-air, SenseNova U1.6 self-correcting image, translation Hy-MT3, video MAGI-2.
- Agent tooling maturity: Coding agents ranked by merge rates / usage (Claude Code leading), PR automation, realistic benchmarks.
- Free/low-cost compute stable (Kaggle primary); new preemptible options (Together AI 50% discount); managed + local stacks remain key. Always independently verify benchmarks, licenses, VRAM needs, and availability.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber/specialized models, access is often restricted. Community licenses may exclude regions or restrict commercial use.*
