# Current AI Briefing

**Last updated:** 2026-11-15

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24-48h (Nov 14-15)
- **Unsloth Dynamic V3.1 GGUFs for Qwen3.8-27B** (Nov 11, ongoing high traction): Highest accuracy GGUFs using updated Dynamic V3.1 algorithm. 5–10% average accuracy gains vs prior UD3 and competitors (GSQ-RCO, Exllama-v3) across Terminal Bench, DeepSWE, LiveCodeBench and more. Quants from 2-bit to 6-bit updated (3-bit unchanged as on par). Smallest ~6GB 1-bit runs on 12GB RAM setups. Strong agentic coding and vision performance retained. Available on HF (`unsloth/Qwen3.8-27B-GGUF`); also for DeepSeek-V4.1-Flash and Qwen3.8-Flash-Next. Blog + benchmarks published.
- **Weight-space programming advances** (recent HF post): Weight space programming lifts Qwen 3.5 0.8B from 7.4% to 58.7% on Math 500. Weights and details shared; continues interest in direct weight editing techniques without full retraining.
- **BananaMind/BETU-SLM-Leaderboard** (recent): Simple leaderboard for small language models. Scores by Overall Index (weighted Hellaswag, ARC Easy, PIQA, Arithmark 3, Tiny Theory of Mind, BananaMind Base Bench). One-command addition of custom models.
- **Ling-3.2-flash free route** (Nov 13-14): Full 1,048,576-token context free on OpenRouter (`inclusionai/ling-3.2-flash:free`, $0/$0). Limited-time vendor benefits; weights not yet on HF.
- **Inkling 2 Small weights fully live** (Nov 12 update): Thinking Machines 594B/17B multimodal MoE under Apache 2.0 on HF. Day-0 vLLM/SGLang/Unsloth support. Strong open model rankings in Agent/Code Arena.

### Ongoing traction & recent
- MiniMax H3-Image continues dominating HF trending (native 4K T2I + multi-ref editing, open weights with regional exclusions; ComfyUI/Diffusers native).
- Google Gemini 4 Hydrogen (fast agentic, 1M context, $1.50/$7.50, xhigh thinking) widespread availability including free AI Studio tiers; strong speed claims.
- Claude Fable 5.2 remains top-ranked on several indexes (AA ~65, BenchLM high).
- Kimi K3.1 Pro, Arete-27B, Edge0 latent MoEs, Ripple-65B-Preview, LTX-2.5, idol (image-to-3D) high activity.
- llama.cpp v1.0.0 stabilizes local inference foundation.

## Hugging Face & Ecosystem Updates
- Trending (as of Nov 15): MiniMaxAI/MiniMax-H3-Image leading image space, xtools-at/DeepSeek-V4-Pro-Qwen3.5-9B-UNCENSORED-heretic, unsloth/Qwen3.8-27B-GGUF (Dynamic V3.1), thinkingmachines/Inkling-2-Small, NousResearch/Arete-27B, moonshotai/Kimi-K3.1-Pro, Zyphra/ZONOS3-Mini (TTS), black-forest-labs/flux-3-image-klein-comfy, speridlabs/idol.
- Ecosystem: Unsloth Dynamic V3.1 improving local quant accuracy for Qwen3.8 family; Diffusers 0.43 day-0 for H3-Image/PAN 2/etc.; Transformers updates for Inkling2/LFM3; live weather model leaderboard; token pooling-aware training for embeddings.
- HF Posts highlight Dynamic GGUFs, weight-space programming, SLM leaderboards, and global weather model rankings.

## Research (recent arXiv / HF Papers ~Nov 12-15 focus)
- High volume in agents, efficiency, multimodal: SO-Arena (System One model reliability), decision models as actor/judge/teacher for long-horizon agents, PixVid (lifting latent video diffusion to pixel space), PhysLoop (LLM physics awareness for video gen), unbundling multimodal vision encoding, BitDecoding-FP4 for native FP4 KV cache, RidgeFill for faster prefill.
- Themes: agent reliability and harness design, efficient local/quantized inference, world models and video generation, system-one vs reasoning models, open decision models.
- Ongoing: weight-space programming, AlphaGenome 2 genomics traction.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (as of Nov 15 2026):**
- Kaggle: ~30 GPU hours/week (T4x2 or P100, 12h sessions).
- Modal: $30 free compute credits/month (Starter, no fee, GPU concurrency).
- Daytona: $200 free compute for new accounts (sandboxes for agents).
- Lightning AI: free credits/hours + Studio.
- Hugging Face ZeroGPU: shared high-end GPU minutes/day for Spaces demos.
- NVIDIA NIM free endpoints, Groq, Google AI Studio (Gemini Hydrogen free tier), OpenRouter (incl. free Ling-3.2-flash 1M), Cloudflare Workers AI (10k neurons/day), SambaNova free tiers.
- AMD Developer Cloud $100 MI300X credit (approved); various startup GPU/API credits (RunPod, Lambda, Google/AWS/Azure, GMI Cloud, fal, Together AI, Baseten).
- Local: llama.cpp v1.0.0 + Unsloth Dynamic V3.1 GGUFs for high-accuracy Qwen3.8-27B on 12GB+; FreeToken/edge0 for large MoEs; vLLM/SGLang/ComfyUI/Diffusers for new releases.

**Hosting & tools:**
- Open weights: MiniMax-H3-Image (4K image), Inkling 2 Small, Kimi K3.1 Pro, Arete-27B, Edge0-145B available for self-host (check licenses/VRAM).
- Coding agents: Claude Code, Cursor, Codex, Copilot, Antigravity, Cline dominant.
- Inference serving: Baseten (top ranked managed APIs with free plan), BentoML, NVIDIA Triton (open-source); llama.cpp 1.0.0 for stable local; day-0 for new models.
- Video/image/world: H3-Image native 4K, PAN 2, LTX-2.5, ZONOS3-Mini TTS.

## Trending Themes
- Local quant accuracy leap: Unsloth Dynamic V3.1 delivers measurable 5-10% gains on agentic benchmarks for popular Qwen3.8-27B, making high-quality local coding more practical on consumer hardware.
- Fast open image generation: MiniMax H3-Image continues to lead HF trending with practical native 4K + multi-ref editing.
- Open decision and small models: Inkling 2 Small weights live; BananaMind SLM leaderboard; free Ling routes.
- Frontier speed/price: Gemini 4 Hydrogen as accessible fast agentic model; Fable 5.2 retains top ranks.
- Accessible free/local compute and coding agents remain foundational; HF trending led by image models, uncensored variants, local MoEs, and improved GGUFs.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber/specialized models, access is often restricted. Community licenses may exclude regions or restrict commercial use.*
