# Current AI Briefing

**Last updated:** 2026-11-17

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24h (Nov 16-17)
- **Alibaba Qwen4-Max** (Nov 16, 2026): Full production release of the Qwen4 flagship MoE. ~2.4T total parameters / 71B active per token, native vision (text/image/video input), 1M-token context. Pricing $1.50 input / $4.50 output per M tokens (down from Qwen3.8-Max). Alibaba reports stronger Work360 performance with ~35% fewer tokens and ~60% lower cost per task; ranks 6th on Code Arena. Available on QwenCloud API, Token Plan, QwenWork, QwenStudio. Smaller open-weight Qwen4 models promised. 1M free quota for 90 days on some plans.
- **Tencent Hy4 flash** (Nov 16, 2026): Lowest-cost Hy model so far. 224B total (incl. 64B Engram) / 12B active, natively multimodal, 1M context. Extremely cheap API: $0.07 input / $0.281 output per M tokens on TokenHub. Weights and OpenRouter listing promised later. Available in WorkBuddy and Yuanbao.
- **Meituan LongCat-Video-Avatar 1.6** (Nov 15, 2026): Open-source (MIT) audio-driven human video generation framework. Improved lip movement, facial/body expressiveness, and long-video consistency (videos >10 min). Weights + technical report on Hugging Face / ModelScope. Ranked high in internal human preference studies.
- **HF Blog highlights** (Nov 17): Agent Safety Tests Belong at the Tool Boundary (red-team evaluation of agent tool use); XYBench (detecting mistaken premises and redirecting to real goals).

### Ongoing traction & recent
- MiniMax H3-Image continues strong HF trending (native 4K T2I + multi-ref editing).
- Unsloth Dynamic V3.1 GGUFs for Qwen3.8-27B: 5–10% accuracy gains on agentic benches; runnable on 12GB RAM.
- Inkling 2 Small open weights (Apache 2.0) on HF with day-0 serving.
- llama.cpp v1.0.0: stable semantic versioning foundation for local inference.
- Gemini 4 Hydrogen: fast agentic model widely available including free tiers.
- LongCat-2.5 (MIT, large multimodal agent MoE trained on Chinese hardware) continues traction.

## Hugging Face & Ecosystem Updates
- Trending (as of Nov 17 ~04:44 UTC): 
  1. xtools-at/DeepSeek-V4-Pro-Qwen3.5-9B-UNCENSORED-heretic (text-gen, high likes/downloads)
  2. MiniMaxAI/MiniMax-H3-Image (text-to-image)
  3. Qwen/Qwen3.8-27B (image-text-to-text)
  4. Lightricks/LTX-2.5 (image-to-video)
  5. Comfy-Org/MiniMax-H3-Image
  6. Zyphra/ZONOS3-Mini (TTS)
  7. higurashi-ai/Haru-4B (audio-to-audio)
  8. thinkingmachines/Inkling-2-Small
  9. unsloth/Qwen3.8-27B-GGUF
  10. speridlabs/idol (image-to-3D)
- Ecosystem: Continued rapid support for new multimodal models in Diffusers/ComfyUI; local quant improvements; open agentic MoEs gaining traction. Unsloth posting highest-accuracy GGUFs.

## Research (recent arXiv / HF Papers ~Nov 16-17 focus)
- High volume in agents, efficiency, multimodal/world models, and AI-for-science.
- Notable HF Blog: Tool-boundary safety for agents; XYBench for premise detection.
- Themes: Chinese flagship efficiency and open multimodal (video avatars, agents), novel generation techniques, local inference maturity (llama.cpp 1.0), AI safety at agent tool use.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (as of Nov 17 2026):**
- **Kaggle Notebooks**: ~30 GPU hours/week (or higher) on P100 or 2×T4, sessions up to 12h. Most predictable free GPU quota.
- **Google Colab free**: T4 (when available), sessions ≤12h, unpublished/fluctuating quota; prioritizes active use. Stops when tab closed.
- Modal: $30 free compute credits/month.
- E2B: one-time $100 usage credits on free Hobby plan.
- Hugging Face ZeroGPU: shared high-end GPU minutes/day for Spaces demos.
- Lightning AI free credits/Studio, NVIDIA Build free serverless inference endpoints, Groq, Google AI Studio (Gemini Hydrogen + Gemma free tiers), OpenRouter (free Ling-3.2-flash 1M context and others), Cloudflare Workers AI (10k neurons/day).
- AMD Developer Cloud $100 MI300X credit (approved developers); various startup GPU/API credit programs (RunPod, GMI Cloud, fal, Together AI, Baseten, etc.).
- Local: llama.cpp v1.0.0 + Unsloth Dynamic V3.1 GGUFs for high-accuracy Qwen3.8-27B on 12GB+; FreeToken/edge for large MoEs; vLLM/SGLang/ComfyUI/Diffusers for new releases. Tools like gpu-free-serve for tunneling free Colab/Kaggle GPUs as local OpenAI endpoints.

**Hosting & tools:**
- Open weights: LongCat-Video-Avatar 1.6 (MIT), MiniMax-H3-Image (4K image), Inkling 2 Small (Apache 2.0), LongCat-2.5, Kimi K3.1 Pro, Arete-27B available for self-host (check licenses/VRAM).
- Coding agents: Claude Code, Cursor, Codex, Copilot, Antigravity, Cline dominant.
- Inference serving: Baseten (top ranked managed APIs with free plan), BentoML, NVIDIA Triton (open-source); llama.cpp 1.0.0 for stable local; day-0 for new models.
- Video/image: H3-Image native 4K, LongCat-Video-Avatar 1.6, LTX-2.5, ZONOS3-Mini TTS.

## Trending Themes
- Chinese flagships accelerating with strong price/efficiency plays: Qwen4-Max and ultra-cheap Hy4 flash, plus open LongCat video/avatar and agent models.
- Local quant accuracy and open agentic MoEs (Unsloth GGUFs, Inkling, uncensored variants) making frontier-adjacent capability more accessible on consumer/edge hardware.
- Agent safety and evaluation (tool boundaries, premise detection) gaining focus as agents proliferate.
- Free/low-cost compute and HF trending remain led by image models, uncensored local variants, and practical open weights. Kaggle preferred for predictable free GPU hours.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber/specialized models, access is often restricted. Community licenses may exclude regions or restrict commercial use.*
