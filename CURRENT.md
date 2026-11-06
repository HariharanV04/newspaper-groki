# Current AI Briefing

**Last updated:** 2026-11-06

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24h (Nov 5-6)
- **OpenAI GPT-6 Cyber**: Specialized cybersecurity model for authorized vulnerability research and exploit development. Scores 48.5% on ExploitGym (up from 32.1% for GPT-5.6 Cyber). Researchers used it to find 81 previously unknown high-severity Firefox vulnerabilities and develop 948 working Linux kernel exploits (including many previously unknown). Rated "Critical" under OpenAI's Preparedness Framework. Available initially to approved Daybreak Red customers via API/Codex. Pricing ~$20/$100 per M tokens. Stronger adherence to authorized scope (near-zero out-of-bounds).
- **Google Gemini Omni 1.2 Flash**: Generally available. Extends native video clips to 15 seconds (from 10), 30% lower pricing ($0.07/s for 720p), better reference adherence. For video generation/editing.
- **Thinking Machines Inkling 2 Small**: 594B total / 17B active MoE. Scores 31 on Artificial Analysis Intelligence Index. Apache 2.0 weights planned; runs on Tinker.
- **Kimi K3.1 Pro (Moonshot AI)**: Open weights fully live and dominating HF trending. 2.8T total / 104B active multimodal MoE, 1M context, MXFP4. Tops open-weight on Agent Arena (#1 open, #13 overall) on 17.5K+ real long-horizon sessions (+5.1% net). Near frontier on Terminal-Bench 4.0 (~65.7). Strong Bash reliability, coding, work/chat. ~1.56TB weights; vLLM/SGLang/Huawei support. Custom license.
- **Ripple-65B Preview (Ricursive)**: Dense 65B Apache 2.0, self-reported US open-weight SOTA on Terminal-Bench 2.1 (80.5). High interest for efficient agentic coding.
- **Tencent Hy4**: Full release with visual understanding and computer-use (CLI + GUI, trained on Blender/CAD etc.).

### Ongoing traction & recent
- Mistral Large 4 continues high HF activity as efficient 1T open multimodal MoE for coding/cyber defense.
- NVIDIA Cosmos 3 open models for interactive world simulation.
- Baidu ERNIE 5.5 Flash Base (280B MoE / 14B active) open-source.
- HF trending: moonshotai/Kimi-K3.1-Pro leading, LTX-2.5, Nemotron Transcribe, Mistral Large 4, Qwen3.8-27B.
- Community: Quantized variants, GGUFs, agent fine-tunes circulating.

## Hugging Face & Ecosystem Updates
- Trending / high activity (Nov 5-6): moonshotai/Kimi-K3.1-Pro (top), Lightricks/LTX-2.5, nvidia/NVIDIA-Nemotron-3.5-Transcribe-30B-A4B, mistralai/Mistral-Large-4, Qwen3.8-27B, Pika-H3-Flex.
- Blog: SuperCLUE split leaders for evaluation, Phonon on-device TTS framework, Dharma Field Extractor (schema-first docs), Palette (IBM slide gen), Clover block-diffusion agents.
- Ecosystem: TRL fine-tuning support for large MoEs (incl. Mistral Large 4 on single node), Transformers/Diffusers/vLLM/SGLang day-0 support for new models, llama.cpp FP8.

## Research (recent arXiv / HF Papers ~Nov 5-6 focus)
- HF Daily Papers: "Turns Matter: Advancing Streaming Video RL via Turn-Level Credit" leading; papers on native Vision-Language-Action policies, adaptive task refresh for self-improvement, efficient diffusion VLMs.
- Agent & long-horizon: Memory compression for agents, criteria exposure in embodied self-improvement, multi-hop reasoning on knowledge graphs, self-hosted AI stacks.
- Efficiency & infra: Low-bit inference, quantized VLMs for edge, training-free sparse attention variants.
- Other: Scientific automation (ChemE-as-Code), anomaly detection, ML repo migration benchmarks.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (verified ~Nov 5-6 2026):**
- Google Colab free tier, Kaggle Notebooks (~30 GPU-h/week T4x2/P100), Hugging Face ZeroGPU (shared Blackwell for Spaces).
- NVIDIA NIM (build.nvidia.com): Free endpoints for many open models (Nemotron, GLM, DeepSeek, etc.).
- Groq free tier, Google AI Studio / Gemini free (Flash family + Omni), Cloudflare Workers AI, SambaNova, OpenRouter free models, Modal ($30/mo free + startup credits).
- Local: FreeToken (GPU+CPU+RAM pooling for large MoEs), Ollama, llama.cpp (FP8), MLX, vLLM/SGLang.
- Coding agents free tiers: GitHub Copilot Free, Cline, Kilo Code, opencode, Google Antigravity, etc.
- Startup credits: Modal up to $25k, various cloud/AI platforms.

**Hosting & tools:**
- Open weights of Kimi K3.1 Pro (massive), Ripple-65B, Mistral Large 4 available for self-hosting or low-cost endpoints. Multi-node or heavy quant for largest.
- Video: Gemini Omni 1.2 Flash API, Pika H3 Flex, LTX-2.5 open weights + Diffusers/ComfyUI.
- Coding agents: Cline (top open), Cursor, Claude Code, OpenAI Codex, Google Antigravity trending.
- Inference optimization: Together compiler, llama.cpp FP8, TRL LoRA for 1T models.
- Cloudflare Pages + Workers for free AI app hosting.

## Trending Themes
- Open-weight frontier agents closing gaps (Kimi K3.1 Pro dominating HF and Agent Arena; Ripple-65B efficient dense coding).
- Specialized closed cyber models (GPT-6 Cyber for authorized vuln research) with strong alignment to scope.
- Video generation advancing (longer clips, lower cost with Omni 1.2 Flash).
- Accessible free/local inference and coding agents keeping capabilities open to developers.
- Research on agent memory, self-improvement, efficient inference, and evaluation frameworks.
- Inference stacks (vLLM/SGLang day-0, TRL) reducing barriers to large open models.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber models, access is heavily restricted to authorized users.*
