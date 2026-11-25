# Current AI Briefing

**Last updated:** 2026-11-25

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24h (Nov 24-25)
- **Z.ai / Zhipu GLM-5.4** (Nov 23-24): First flagship Loop Transformer. Runs 28 layers of the GLM-5 base twice (shared weights) for deeper reasoning at ~750B scale, claimed to reach intelligence comparable to 2T-3T models. 1M context, native multimodal (vision/video/text/files), focused on generalized coding. Hosted; open weights planned after safety. Day-0 interest high.
- **Baidu ERNIE 5.5 Flash Preview** (Nov 23-24): 280B MoE (14B active), 1M context, tool calling. Apache 2.0 weights on HF/ModelScope (post-trained checkpoint; base has restrictions). Day-0 vLLM support via plugin. Thinking modes (low/medium/high). FP8/FP4/BF16 options + speculative decoding.
- **PrismML Ternary Bonsai 2.5 27B** (Nov 24): Open weights GGUF. Ternary quantization (~5.9GB footprint). Tuned for long agent runs (fewer turns/tokens). Built on Qwen3.8-27B; SWE-bench Verified gains (60.8 → 75.6). Runs on NVIDIA/Intel via llama.cpp, Macs via MLX.
- **Ant Group / inclusionAI Ling-3.2-air** (Nov 23-24): Open MIT multimodal MoE (124B total / 5.5B active), 1M context (native 262K). Strong on agentic/terminal/document benchmarks. Weights on HF.
- **Tencent Hy-MT3** (Nov 24): Open Apache 2.0 translation models (1.8B/7B/30B-A3B). 102 languages (up from 38). FP8/GGUF, vLLM/SGLang. Improved real-world translation (fewer errors/omissions).
- **SenseTime SenseNova U1.6** (Nov 24): 8B unified image understand/generate/edit with self-correction (draws, checks, fixes blur/typos). Apache 2.0 + LoRAs/FP8/GGUF/ComfyUI.
- **NVIDIA Nemotron-Labs-Image-30B-A3B**: New open-weight visual AI model on HF.
- **Sand AI MAGI-2**: 480B parameter video generation (Multi-Head Latent MoE), 1080p with native audio, up to 30s, multi-reference. Open weights coming soon. Founded by former MSRA researcher.
- **Inkling 2 Mini** (still heavily trending): Open Apache looped MoE (~26B total / 3B active), multimodal 1M context, local-friendly. #1 trending on HF with massive GGUF downloads.
- **Other**: Cognition SWE-2.1 coding model (RL on Kimi K3, free for Devin tiers); Google Humanity's First Exam for LLM reliability + Cloud Agent Gateway; Anthropic Claude Ship beta for PR review/fixes; OpenAI GPT-6.2 variants ongoing; Transformers v5.24.1 patch for vLLM compatibility.

### Hugging Face trending (as of Nov 25)
thinkingmachines/Inkling-2-Mini and unsloth/Inkling-2-Mini-GGUF (millions of downloads), inclusionAI/Ling-3.2-air, baidu/ERNIE-5.5-Flash-Preview, prism-ml/Ternary-Bonsai-2.5-27B-GGUF, tencent/Hy4-flash, Lightricks/LTX-2.5, apple/DepthPro2 / FastFrames-L. Strong activity on looped/efficient local models, MoE, agent adapters, and visual models.

## Hugging Face & Ecosystem Updates
- Transformers v5.24.1: Fixes for vLLM compatibility, distributed workflows, Llama 4 / Dory, audio encoder.
- HF Blog: Loop-Behind Decoding (overlapping recurrent work in looped models), Wonder Agent (on-device child-friendly AI design), Decision Models for document AI, harness-specific RL for agents.
- Day-0/strong support for new open models (ERNIE, Ling, Bonsai, Inkling, Hy-MT3) across Transformers, vLLM, SGLang, Unsloth, llama.cpp, MLX.
- Local/edge accessibility accelerating with ternary/quantized efficient models.

## Research (recent arXiv / HF Papers ~Nov 24-25 focus)
- LoopDVR: Looped Transformer for efficient dense visual recognition (Nov 24).
- Disclosure Bias in AI Reviewers: AI models systematically score papers lower when authors disclose AI involvement (arXiv 2611.30410).
- SLAKE: Training-free method for long-context efficiency and memory reduction.
- Coding4Games, PartAgent (agentic 3D segmentation), Clinical3D-Bench, SWE-2.1 technical details.
- Ongoing: agent skill learning, long-context, quantization, medical decision models, formal verification (Claude VP ≠ VNP Lean claim still unverified by humans), alphaXiv autonomous agent-generated preprints.
- Broader: Efficiency of looped/MoE architectures, memory systems, agentic science, multimodal.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (as of Nov 25 2026):**
- **Kaggle Notebooks**: ~30 GPU hours/week on 2×T4 (sessions ≤12h). Most reliable free quota for experiments/fine-tuning. Phone verification. No card.
- Google Colab free: T4 when available, session/quota limits.
- Hugging Face ZeroGPU: Short daily shared high-end GPU minutes (5 min free) for Gradio Spaces (PRO much more). Demo-oriented.
- Modal: $30 free credits/month on Starter.
- Lightning AI: Free credits / studios (up to ~50 GPU hours).
- E2B sandboxes: One-time $100 usage credits on Hobby (no card).
- Cloudflare Workers AI, Groq free tier, Google AI Studio, OpenRouter free models, NVIDIA NIM free endpoints, ModelScope, Paperspace Gradient (public projects), Baidu AI Studio.
- Cheap paid: Shadeform marketplace H100 from ~$2.73/hr; RunPod/Lambda competitive.
- Startup/student programs: Thunder Compute $20, Crusoe, Inference.net grants, etc. Fireworks AI free training for select models through Nov 30.
- Local: llama.cpp, Unsloth GGUFs (Inkling, Bonsai ternary, Qwen), MLX. Inkling 2 Mini and Ternary Bonsai practical on consumer hardware.

**Hosting & tools:**
- Open weights gaining: ERNIE 5.5 Flash, Ling-3.2-air, Ternary Bonsai, Hy-MT3, SenseNova U1.6, Inkling Mini.
- Coding/agent tools: Claude Code (still top-ranked for most devs, high merge rates), OpenAI Codex, Cursor, GitHub Copilot, Devin, Google Antigravity, Cline, OpenCode. Cognition SWE-2.1. Anthropic Claude Ship for PR automation.
- Inference: Strong day-0 support (vLLM for ERNIE, etc.). Unsloth for local fine-tuning.
- Security tooling: Shirudo (OpenAI+Cisco) for agent eBPF shields continues relevant.

## Trending Themes
- Loop Transformer architectures: GLM-5.4 (large-scale flagship), Inkling 2 Mini (local dominant on HF), others — deeper reasoning via repeated shared-layer passes.
- Efficient open local models: Ternary quantization (Bonsai 5.9GB), looped MoEs, GGUF dominance.
- Open multimodal and specialized: Ling-3.2-air, SenseNova U1.6 self-correcting image, translation Hy-MT3, video MAGI-2.
- Agent tooling maturity: Coding agents ranked by merge rates / usage (Claude Code leading), PR automation, realistic benchmarks.
- Free/low-cost compute stable (Kaggle primary); managed + local stacks remain key. Always independently verify benchmarks, licenses, VRAM needs, and availability.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber/specialized models, access is often restricted. Community licenses may exclude regions or restrict commercial use.*
