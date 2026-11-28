# Current AI Briefing

**Last updated:** 2026-11-28

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24h (Nov 27-28)
- **NVIDIA Nemotron-Labs-Image-30B-A3B**: Open weights for autoregressive image generation model (30B total / 3B active MoE). "Pixel as Code" approach in Nemotron-Labs-VisualCreation framework. Non-commercial research/evaluation only. Vendor benches: GenEval 92.86 (vs GPT Image 2 89), LongTextBench 97.98 (vs 96). On HF.
- **inclusionAI / Ant Group Ling-3.2-air**: Open MIT multimodal MoE (124B total / 5.5B active across 512 experts). Accepts text, images, video. Strong benchmark card published. On HF.
- **Sber GigaChat 4**: Two open MoE models — 708B total / 41B active (MIT license, 1M context, instant + reasoning modes) and 37B total / ~4B active (non-commercial). Technical report available.
- **Lightricks LTX-2.5**: Updated with multishot capabilities and diffusion decoder. Image-to-video continues trending heavily.
- **inclusionAI Ming-Image-0.2-Design**: MIT 6B DiT text-to-image for visual design; claimed top among open-weight on AA-Image-T2I leaderboard.
- **Tencent Hy3D 3.6**: 3D generation (up to 2M faces, 8K PBR textures) on TokenHub. Free daily generations available.
- **prism-ml Ternary-Bonsai-2.5-27B-GGUF**: Continues climbing HF trending. Ternary quantization of Qwen3.8-27B (~5.9GB at 1.76 bits/weight). Near full-precision tool-calling; Apache 2.0 for llama.cpp/MLX.
- **Inkling 2 Mini** (Thinking Machines): Still #1 trending on HF (trending score ~1.2k-1.4k). Open Apache looped MoE (~26.4B/5.4B active), multimodal. Unsloth GGUF variants with millions of downloads. Local-friendly.
- Other: WeMM-Ecom family (Tencent, Apache multimodal e-commerce 2B-35B), ERNIE-5.5-Flash-Preview (Baidu), various GGUF/abliterated variants.

### Hugging Face trending (as of Nov 28)
1. thinkingmachines/Inkling-2-Mini
2. unsloth/Inkling-2-Mini-GGUF (millions of downloads)
3. SulphurAI/Sulphur-3
4. prism-ml/Ternary-Bonsai-2.5-27B-GGUF
5. AtomicChat/Inkling-2-Mini-Uncensored-GGUF
6. inworld/voice-isolator
7. Lightricks/LTX-2.5
8. llamaindex/OCRia-nano-1
9. nvidia/Nemotron-Labs-Image-30B-A3B (rising)
10. ISTA-DASLab/Inkling-2-Mini-GSQ-RCO-GGUF

Strong activity on efficient local/quantized models (Inkling variants, ternary), image/video generation, and audio isolation.

## Hugging Face & Ecosystem Updates
- HF Blog: Trainium3 experiments with LTX-2.5 video generation; multi-agent training (shared small model for private info exchange); Nemotron Parse 3.5 document extraction pipeline; llama.cpp benchmark dashboard for AMD.
- Day-0/strong support continues for new open models across Transformers, vLLM, SGLang, Unsloth, llama.cpp, MLX.
- Local/edge accessibility accelerating with ternary/quantized efficient models and GGUF dominance. Inkling Mini and Ternary Bonsai practical on consumer hardware / single high-end GPUs.

## Research (recent arXiv / HF Papers ~Nov 27-28 focus)
- **Stable Gated DeltaNet-2**: Understanding and Mitigating Recurrent State Instability (top HF Daily Papers). Symmetric erasure and decay-regulated writing stabilize recurrent states for long-context.
- **OS-Omni**: Benchmarking Generalist Computer-Using Agents on Long-Horizon Workflows Across Platforms (Windows, Ubuntu, macOS, iOS, Android, Web).
- ProxyGenBench: Proxy-guided video generation.
- Solve Vision with Code: Coding agents as stronger visual reasoners than pure video models.
- Sage-Med: Scaling Medical Multimodal Intelligence (Shanghai AI Lab, strong on 31 public multimodal benchmarks).
- Mixture-of-Loops Transformer and related efficiency papers.
- Broader: Agent benchmarks, long-horizon computer use, recurrent/linear attention fixes, medical VLMs, visual generation.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (as of Nov 28 2026):**
- **Kaggle Notebooks**: ~30 GPU hours/week on 2×T4 (sessions ≤12h). Most reliable free quota for experiments/fine-tuning. Phone verification. No card.
- Google Colab free: T4 when available, session/quota limits (not guaranteed).
- Hugging Face ZeroGPU: Short daily shared high-end GPU minutes (5 min free) for Gradio Spaces (PRO much more). Demo-oriented.
- Modal: $30 free credits/month on Starter.
- Lightning AI: Free credits / studios (up to ~50 GPU hours).
- E2B sandboxes: One-time $100 usage credits on Hobby (no card).
- Cloudflare Workers AI, Groq free tier, Google AI Studio (Gemini free tier), OpenRouter free models, NVIDIA NIM free endpoints, ModelScope, Paperspace Gradient.
- Fireworks AI: Free training of Muse Glimmer 30B (SFT/DPO/RL) through Nov 30.
- Startup/student programs: Thunder Compute $20, Anyscale $100 signup, various GPU credits (GMI Cloud, Runpod, Lambda for YC, NVIDIA Inception, Vast.ai match).
- Local: llama.cpp, Unsloth GGUFs (Inkling, Bonsai ternary, Qwen), MLX. Strong options for consumer hardware.

**Hosting & tools:**
- Open weights gaining: Nemotron Image, Ling-3.2-air, GigaChat 4, Ternary Bonsai, Ming-Image, WeMM-Ecom, Inkling Mini.
- Coding/agent tools: Claude Code, OpenAI Codex, Cursor, GitHub Copilot, Devin, Google Antigravity, Cline remain dominant. Multi-agent frameworks advancing.
- Inference: Strong support for new open models. Unsloth for local fine-tuning. TRL for distillation/SFT.

## Trending Themes
- Efficient open local models: Ternary quantization (Bonsai ~6GB), looped MoEs (Inkling Mini dominant on HF), GGUF dominance for consumer hardware.
- Autoregressive / agentic image and video generation (Nemotron Pixel-as-Code, LTX-2.5, Ming Design).
- Open multimodal MoEs under permissive licenses (Ling-3.2-air MIT, GigaChat 4).
- Agent benchmarks and computer-use (OS-Omni, long-horizon workflows).
- Recurrent/linear attention improvements (DeltaNet-2) for long context efficiency.
- Free/low-cost compute stable (Kaggle primary); local stacks remain key for privacy and cost. Always independently verify benchmarks, licenses, VRAM needs, and availability.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber/specialized models, access is often restricted. Community licenses may exclude regions or restrict commercial use.*
