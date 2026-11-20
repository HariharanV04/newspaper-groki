# Current AI Briefing

**Last updated:** 2026-11-20

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24-48h (Nov 18-20)
- **Google Gemini 4 Neon** (Nov 18, 2026; detailed Nov 19-20): Mid-tier Gemini 4 model adapted from Carbon. Frontier-level for complex software engineering, knowledge work, and science with fast task completion. 1M-token context (text/image/video/audio/PDF input, text out), four thinking levels (low/medium/high/xhigh). Pricing: $3 input / $0.15 cached / $15 output per M tokens. Ranks ~61 on AA Intelligence Index (xhigh, 3rd overall), #1 on AA Coding Agent Index (58.6), strong on Vals (70.9% #2), Terminal-Bench 4.1 (65.2%), Agents' Last Exam, science/math benches. Cost per task ~17-32% lower than Carbon. Available in Gemini API/AI Studio, Antigravity (Pro/Ultra), Gemini app (replaces Argon), GitHub Copilot. No free tier.
- **RadixArk DaisyRose-27B** (Nov 18): First model from RadixArk. Built on Qwen3.8-27B, RL-trained (Miles) on ~1,200 curated long-horizon agent tasks (sessions to 1M tokens) over 18 days on 144 H200s. Improves Terminal-Bench 4.1 pass@1 from 5.6% to 12.0%; gains across coding, reasoning, IF, SWE-bench Pro. Apache 2.0 weights (BF16/FP8/NVFP4), retains 256K context + image input. Efficient post-training example.
- **Reson8 Rumble-2-Flash** (Nov 18, highlighted): Open Apache 2.0 0.5B speech ASR for 40+ languages with auto detection. Native in Transformers/vLLM. Competitive WER with much larger models (e.g. near Nemotron 3.5 Transcribe 30B on call-center bench; strong multilingual Open ASR). Extremely fast (~7000+ RTFx). Ideal for edge/deploy.
- **OVHcloud Olala mini 7A1B** (Nov 19): Open Apache 2.0 hybrid Mamba-3/attention MoE (~6.8B total / ~1B active), 32K context reasoning model. Released at OVH AI Summit on HF.
- **Microsoft Aion 1.0 Instruct** (Nov 18): 2.3B open MIT on HF (32K, 8 languages); optimized version for Windows OS SLM by early 2027.
- **Phancy Phai-A1** (Nov 18): Open Apache coding/agent model post-trained from Qwen, 1M context, Ascend-runnable.
- **Tencent Hy4 flash** open weights (Nov 17-18, still strong): 220B MoE / ~12B active multimodal 1M context under Tencent Hy License. Trending heavily on HF.
- **OpenAI GPT-Live-1.1** (Nov 19-20): Improved full-duplex voice model in Live API — better transcription, consistent accents, cheaper standby ($0.02/min). Background mode discounts up to 40% on GPT-6.2.
- **Google Genie 4**: Interactive world model now available via Gemini API / AI Studio for continuous 720p worlds at 24fps with audio.
- Ongoing: GPT-6.2 Astra/Sol (Nov 17, cheaper 1.05M context), MAI Code 2 family (Nov 17), SenseNova-Loop-9B, Apple FastFrames-L (text-to-video), MiniMax-H3-Image, etc.

### Hugging Face trending (as of Nov 20 ~04:45 UTC)
1. higurashi-ai/Haru-4B (audio-to-audio)
2. tencent/Hy4-flash (image-text-to-text)
3. apple/FastFrames-L (text-to-video)
4. harness-hub/Qwen3.8-27B-pi-adapted (agent LoRA)
5. inworld/voice-isolator
6. Qwen/Qwen3.8-27B
7. MiniMaxAI/MiniMax-H3-Image
8. maxwell-model/Maxwell-V1-Flash
9. Lightricks/LTX-2.5
10. chatrlabs/Qwen-Image-2.1-Uncensored-Omni-Quantized
... DaisyRose-27B, Rumble-2-Flash, NVIDIA-Nemotron-3.5-Bolt, etc. also rising.

## Hugging Face & Ecosystem Updates
- Blog: Superfluid Fleet for mixed local inference queues; DaisyRose-27B post-training efficiency lessons; Rumble-2-Flash ASR evaluation patterns; agent safety at tool boundary.
- Diffusers 0.43.0: MiniMax-H3-Image, Pika H3 Flex (video+audio), etc.
- Inference Providers: language models routed via OpenRouter (prices unchanged, no own keys for LMs).
- Day-0 support continuing for new open models; local/edge accessibility rising with small efficient models.

## Research (recent arXiv / HF Papers ~Nov 19-20 focus)
- High volume on agents: memory management (How Much Should an Agent Remember? — self-distilled memory lessons), context as resource for concurrent sessions, self-improving visual agents, scientific problem probing (Pro² Agent).
- World models: learned priors over visual evidence; interactive world modeling under rules (WorldRuler); 4D scene geometry (π⁴).
- Efficiency: Newton-PINet for fast PINNs; speculative decoding improvements; on-policy morphing to hybrid attention.
- AI-for-science: DeepQuest for Alzheimer's knowledge gaps; various physics-informed and robotics (ECHO humanoid control, alignment for robot-use agents).
- Themes: Agent reliability on long-horizon/procedural tasks, parameter-efficient and hybrid architectures, multimodal world simulation, local/edge deployment of capable models.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (as of Nov 20 2026):**
- **Kaggle Notebooks**: ~30 GPU hours/week on P100 or 2×T4 (sessions ≤12h). Most reliable free quota for experiments.
- **Google Colab free**: Limited T4 access, fluctuating.
- Hugging Face ZeroGPU: Short daily shared high-end GPU minutes for Gradio Spaces (PRO much more).
- Modal: $30 free credits/month (Starter).
- E2B: one-time $100 on Hobby plan (agent sandboxes).
- Lightning AI: free credits/Studio (~up to 30-50 GPU hours).
- NVIDIA NIM free endpoints, Groq free tier, Google AI Studio (Hydrogen free), OpenRouter free models, Cloudflare Workers AI (10k neurons/day).
- New/notable: Thunder Compute student $20 free GPU credit (A6000/L40); various startup programs (E2E, GMI Cloud, Runpod, AMD $100, etc.); Fireworks free fine-tuning of Muse Glimmer until Nov 30.
- Local: llama.cpp, Unsloth Dynamic GGUFs, FreeToken for pooling GPU+CPU+RAM on consumer hardware.

**Hosting & tools:**
- Open weights gaining: DaisyRose-27B, Rumble-2-Flash, Hy4-flash, Olala mini, SenseNova-Loop-9B, Phai-A1, FastFrames-L, MiniMax-H3-Image.
- Coding agents: Copilot adding Neon/GPT-6.2/MAI; Antigravity, Claude Code, Cursor, Codex, Devin Desktop (ex-Windsurf), OpenCode trending. Perplexity Brain auto-creates self-improving agent skills.
- Inference: Baseten, BentoML, Triton; vLLM/SGLang/ComfyUI/Diffusers strong day-0 support. AMD ROCm 10.2 updates.
- Video/speech: FastFrames, LTX-2.5, Rumble-2-Flash, Genie 4, Hy4 multimodal.

## Trending Themes
- Rapid Gemini 4 family expansion: Neon fills mid-tier price/performance gap (faster/cheaper than Carbon on many agent/coding/science tasks).
- Efficient open post-training: DaisyRose shows large agent gains from small curated RL data + compute; small ASR (Rumble) and looped/MoE models matching much larger ones.
- Chinese open multimodal efficiency (Hy4 flash) + Apple/others in video gen continuing to trend on HF.
- Agent focus: memory, self-improvement, tool safety, integrated into coding tools and Perplexity-style personal agents.
- Free/low-cost compute stable; managed hosting + local stacks + startup credits remain key for developers. Always cross-check vendor benchmarks independently.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber/specialized models, access is often restricted. Community licenses may exclude regions or restrict commercial use.*
