# Current AI Briefing

**Last updated:** 2026-11-19

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24-48h (Nov 17-19)
- **Google Gemini 4 Neon** (Nov 18, 2026): Mid-tier Gemini 4 model adapted from Carbon. Delivers frontier-level intelligence for complex coding, knowledge work, and science at higher speed/lower cost than top models. 1M-token context (text/image/audio/video input), thinking levels low/medium/high/xhigh. API pricing $3 input / $15 output per M tokens (cached $0.15; batch/flex half price). Ranks strongly on AA Intelligence Index (~61 at xhigh), Vals, Agent Arena. Available in Gemini API/AI Studio, Antigravity (Pro/Ultra), Gemini app, GitHub Copilot. No free tier (Hydrogen has one). Knowledge cutoff ~March 2026.
- **Microsoft MAI family** (Ignite Nov 17): MAI Code 2 (everyday coding, claims 98% of GPT-6.1 Sol quality at ~40% price; 96% of Opus 5.5 at ~5%), Code 2 Flash (high-volume), Cyber 2 Flash (security, strong CyberGym claims), Image 2.7, Realtime 1, Transcribe 2, Decision models. Sparse MoE + vision, 1M+ context for coding models. Available in GitHub Copilot (various tiers); licensed weights for Azure customization. Price-performance push for enterprise agents.
- **OpenAI GPT-6.2 Astra and Sol** (Nov 17): Cheaper successors. Astra ~20% cheaper than prior ($8/$40), Sol everyday work ($2/$10). 1.05M context, text+image, strong agentic/coding. Available in ChatGPT Work, Codex, API, GitHub Copilot. Background-mode beta added.
- **Tencent Hy4 flash open weights** (Nov 17-18): 220-224B MoE (12B active, incl. Engram), multimodal, 1M context. Weights (base/FP8) on HF/ModelScope under Tencent Hy License. Ultra-cheap API previously noted; now open for self-host.
- **SenseTime SenseNova-Loop-9B** (Nov 17): Open Apache 2.0 ~9B multimodal (text/image). Looped architecture (32 layers → 56 executions via shared middle block + mHC) for deeper compute. Competitive with Qwen3.8-27B on agent/data benches (e.g., AIDABench edge). 512K context; 4-bit ~4.9GB, low VRAM (~10GiB at 64K). HF + GitHub.
- **Reson8 Rumble-2-Flash** (highlighted Nov 18): Open 0.5B speech ASR for 40+ languages (Apache 2.0). Matches much larger models on phone calls/ASR leaderboards; efficient for edge/deploy.
- **Phancy Phai-A1** (Nov 18): Fast coding/agent model post-trained from Qwen, 1M context, open weights (Apache), runs on PC/Huawei Ascend.
- Other: Microsoft-Decision-1.1 GA; various smaller open (DaisyRose-27B, etc.).

### Ongoing traction & recent
- MiniMax H3-Image, LTX-2.5, Qwen3.8-27B (and pi-adapted LoRA for agents), Inkling-2-Small, Haru-4B (audio) dominate HF trending.
- Unsloth Dynamic GGUFs and local quant improvements continue.
- Hugging Face Inference Providers now route LM traffic via OpenRouter (price/speed/reliability, fallbacks; :fastest/:cheapest selectors).
- Transformers v5.23.0 with new model support (Inkling2 etc.).

## Hugging Face & Ecosystem Updates
- Trending (as of Nov 19 ~03:44 UTC): 
  1. higurashi-ai/Haru-4B (audio-to-audio)
  2. harness-hub/Qwen3.8-27B-pi-adapted (image-text-to-text, agent LoRA)
  3. Lightricks/LTX-2.5 (image-to-video)
  4. thinkingmachines/Inkling-2-Small
  5. MiniMaxAI/MiniMax-H3-Image (text-to-image)
  6. Qwen/Qwen3.8-27B
  7. tencent/Hy4-flash
  8. n4ze3m/tiny-voca (TTS)
  9. apple/FastFrames-L (text-to-video)
- Blog: Rumble-2-Flash ASR evaluation patterns; agent safety at tool boundary; Modular Diffusers for model ports; OpenRouter routing changes for Inference Providers; CI scaling with llama.cpp.
- Ecosystem: Day-0 support for new models; open agentic adapters (e.g., Qwen pi-adapted doubles SWE-bench Pro scores in some reports); local inference maturity.

## Research (recent arXiv / HF Papers ~Nov 17-19 focus)
- High volume in agents (self-improvement, memory, tool boundaries, long-horizon, multi-agent), efficiency (looped/lattice architectures, quant, speculative decoding), multimodal/world models, AI-for-science.
- Notable: Latent Lattice Language Models (perplexity gains via residual enhancements); agent papers on harness evolution, stale retrieval in memory (StaleBench), trading agents (beta not alpha), GUI backdoors, scientific judgment, self-evolving memory (ARISE). Papers with Code lists Gemini 4 Neon, Clairic open-weights, LoFT video geometry, etc.
- Themes: Parameter-efficient depth (looped models), agent evaluation/safety, Chinese open multimodal efficiency, local/edge accessibility.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (as of Nov 19 2026):**
- **Kaggle Notebooks**: ~30 GPU hours/week (or higher) on P100 or 2×T4, sessions up to 12h. Most predictable free GPU quota.
- **Google Colab free**: T4 (when available), sessions ≤12h, fluctuating quota.
- Modal: $30 free compute credits/month (Starter, no fee).
- E2B: one-time $100 usage credits on free Hobby plan (sandboxes).
- Hugging Face ZeroGPU: limited daily shared high-end GPU minutes for Spaces demos (PRO more).
- Lightning AI free credits/Studio, NVIDIA NIM free serverless endpoints (Developer Program), Groq, Google AI Studio (Hydrogen free tiers), OpenRouter free models, Cloudflare Workers AI (10k neurons/day).
- AMD Developer Cloud $100 MI300X credit; startup programs (fal up to $50k, Together, Baseten, Runpod, GMI Cloud, E2E Networks, etc. up to $100k+). Crusoe, Anyscale credits noted.
- Local: llama.cpp, Unsloth GGUFs for high-accuracy on 12GB+; SenseNova-Loop-9B 4-bit low VRAM; Hy4 flash open; tools for tunneling free GPUs as OpenAI endpoints.

**Hosting & tools:**
- Open weights: Hy4 flash, SenseNova-Loop-9B (Apache), Rumble-2-Flash, Phai-A1, MiniMax-H3-Image, Inkling 2 Small, LongCat variants, Kimi K3.1 Pro (check licenses/VRAM).
- Coding agents/tools: GitHub Copilot adds Gemini 4 Neon, GPT-6.2 Astra/Sol, MAI Code 2/Flash; Codex CLI 0.170.0 adds realtime voice over WebRTC; Claude Code updates (MCP, status); OpenCode model support; Devin pricing/bots; Google AI Studio builds full-stack Android apps from prompts; Pydantic AI, Agents SDK fixes/features.
- Inference serving: Baseten (top ranked managed with free plan), BentoML, NVIDIA Triton (open-source); OpenRouter routing on HF; day-0 for new models. vLLM/SGLang/ComfyUI/Diffusers ongoing.
- Video/image/speech: H3-Image, LTX-2.5, Rumble-2-Flash ASR, Hy4 multimodal.

## Trending Themes
- Frontier price/performance war intensifies: Gemini 4 Neon ($3/$15 mid-tier), Microsoft MAI undercutting rivals on coding/security, OpenAI GPT-6.2 cheaper, Chinese ultra-cheap Hy4 + open weights.
- Parameter-efficient open models (looped 9B matching 27B-class, small ASR, PC-runnable 1M) + local quant accessibility.
- Agent proliferation: safety at tool boundaries, self-improvement, memory, coding agents integrated into Copilot/Codex/etc.; full-stack app gen from prompts.
- HF ecosystem: OpenRouter routing, trending audio/image/video + agent adapters; open weights momentum from Tencent/SenseTime.
- Free/low-cost compute stable; startup credit programs and managed hosting (Baseten et al.) key for developers. Always verify independent benchmarks vs vendor claims.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber/specialized models, access is often restricted. Community licenses may exclude regions or restrict commercial use.*
