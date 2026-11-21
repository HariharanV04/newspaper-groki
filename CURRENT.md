# Current AI Briefing

**Last updated:** 2026-11-21

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24-48h (Nov 20-21)
- **Thinking Machines / Hugging Face Inkling 2 Mini** (Nov 20, 2026): Open Apache 2.0 looped mixture-of-experts multimodal model (~26.4B total parameters / ~3.4B active per token; research variant allows 1-2 loop passes instead of 3 for faster inference). Text + image input, text output, 1M-token context. ~20GB mixed NVFP4/MXFP8 checkpoint designed for local AI (32GB+ Apple Silicon Macs, DGX Spark, etc.). Supports Transformers, llama.cpp, MLX, SGLang. Leads open-weights models under 100B total on several agentic coding and reasoning benchmarks (e.g. DeepSWE, Vals). Available on Tinker for inference/fine-tuning + full weights on HF. Strong local/edge play; looping increases capability without major monitorability loss at this scale.
- **Tencent Hy4 full open weights** (Nov 20): Natively multimodal flagship MoE (770B total / 49B active per token + vision encoder + speculative drafter), 1M context, text/image/video understanding + computer use (CLI + GUI). Released Hy4 (instruct), Hy4-FP8, and pre-trained base. On HF, ModelScope, GitCode under Tencent Hy License 1.0 (Apache-2.0-derived with extra commercial terms for large MaaS providers >$50M revenue or 100M MAU; internal use exempt). Day-0 vLLM + SGLang support, GGUF builds, System Card with safety/security/alignment evaluations (including frontier cyber and bio risks). Previously API-only since Nov 4.
- **Tencent WeMM-Video family** (Nov 20): Four omni-modal models (text/image/audio/video inputs → text outputs) for joint audio-visual understanding. Sizes: 2B, 4B, 9B dense, and flagship 35B-total / 3B-active MoE. Apache 2.0 weights + quantized builds (FP8/AWQ/GGUF/NVFP4). Vendor-reported new open SOTA on omni video understanding (beats prior Qwen3-Omni class on some benches). Technical report Nov 19.
- **Cloudflare Clairic** (Nov 20): Open Apache 2.0 27B model built on Qwen3.8-27B for typed schema filling / structured extraction from text, JSON, or images, plus new 9B Clairic-flash. Ahead of traditional OCR pipelines in Cloudflare tests; flash median latency ~155ms.
- **NVIDIA Nemotron-Labs-Sigma** (Nov 21): 14 open continuous diffusion language model checkpoints.
- Ongoing strong: RadixArk DaisyRose-27B (RL-only agentic on Qwen3.8-27B, Terminal-Bench gains), Reson8 Rumble-2-Flash (0.5B multilingual ASR), Gemini 4 Neon (mid-tier closed, strong coding/agent), GPT-6.2 Astra/Sol, MAI Code 2 family, Hy4-flash (earlier open weights still trending).

### Hugging Face trending (recent)
Inkling-2-Mini and GGUF variants rising fast; Haru-4B (audio), Hy4-flash / Hy4 variants, Qwen pi-adapted agent adapters, LTX-2.5, MiniMax-H3-Image, DaisyRose-27B, Rumble-2-Flash continuing to see high activity.

## Hugging Face & Ecosystem Updates
- Blog highlights: OhanTTS streaming speech for Armenian + multilingual; Superfluid Fleet (mixed local machines as one inference queue); tool-level agent security demos; DaisyRose post-training efficiency; Rumble-2-Flash ASR evaluation patterns.
- Day-0 support strong for new open models (Inkling 2 Mini, Hy4, WeMM-Video) across Transformers, vLLM, SGLang, Unsloth, llama.cpp, MLX.
- Local/edge accessibility accelerating with compact high-capability models (Inkling Mini ~20GB, quantized Hy variants, small ASR).

## Research (recent arXiv / HF Papers ~Nov 19-21 focus)
- **alphaXiv “A Society of AI Scientists”** (announced ~Nov 19-20): 12-week multi-lab experiment with 936 autonomous agents across 35 labs produced 936 preprints (with code/data) on a shared agent preprint server, founded their own Journal of Agent Research, and used executable peer review. Agents overturned headline claims in ~49% of challenged cases when objections were run as code. Agents stronger on rigor than novelty vs matched human preprints. Powered largely by Claude + other models. Archive opened publicly.
- AI-assisted mathematics: Claude credited with key step in machine-verified Riemann Hypothesis work (extending toward GRH, Lean formalization); human-only GRH draft released same period; AI-assisted Navier-Stokes blowup claims with Lean. Terry Tao and others commenting on verification status.
- HF Daily Papers trending: WeVisForensics (self-evolving agent for AI-generated video detection), Mind2Act World (embodied mind-action benchmark for robotics), probing “conscious” mind / global workspace in VLMs, TwinLab-Bench for AI scientists in lab digital twins, various agent memory/efficiency papers.
- Broader themes: Agent reliability and long-horizon work, executable verification, multimodal forensics, efficiency of looped/MoE architectures, local deployment of capable models.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (as of Nov 21 2026):**
- **Kaggle Notebooks**: ~30 GPU hours/week on P100 or 2×T4 (sessions ≤12h). Most reliable free quota for experiments/fine-tuning. Phone verification, no card.
- Hugging Face ZeroGPU: Short daily shared high-end GPU minutes (RTX Pro 6000 Blackwell class) for Gradio Spaces (PRO much more). Demo-oriented.
- Modal: $30 free credits/month on Starter (no monthly fee).
- Cloudflare Workers AI: 10,000 neurons/day (catalog models).
- E2B: one-time $100 on Hobby (agent sandboxes).
- Lightning AI: free credits/Studio (~up to 30-50 GPU hours).
- NVIDIA NIM free endpoints, Groq free tier, Google AI Studio, OpenRouter free models, Colab free (fluctuating).
- Startup/student programs: Thunder Compute student $20 GPU credit, E2E Networks, GMI Cloud, Runpod, AMD AI Developer Program ($100), various GPU grants. Always verify current terms.
- Local: llama.cpp, Unsloth GGUFs, MLX, FreeToken-style pooling. Inkling 2 Mini now practical on consumer unified memory.

**Hosting & tools:**
- Open weights gaining rapidly: Inkling 2 Mini (local-friendly), Hy4 full + flash, WeMM-Video, Clairic, DaisyRose-27B, Rumble-2-Flash, Olala mini, etc.
- Coding agents: Claude Code, Cursor, OpenAI Codex, GitHub Copilot (integrating new models), Google Antigravity, OpenCode, Devin Desktop. Focus on multi-step agents, tool safety, and parallel/background work.
- Inference: Strong day-0 vLLM/SGLang/Transformers/Unsloth support. Local stacks maturing for smaller high-capability models.
- Video/speech/multimodal: WeMM-Video, LTX-2.5, Rumble-2-Flash, Genie 4, Hy multimodal, MiniMax-H3-Image.

## Trending Themes
- Local/edge capable open models: Inkling 2 Mini (~20GB multimodal MoE running on laptops) and compact efficient architectures (looped, small active params) making frontier-adjacent performance practical without cloud.
- Chinese open multimodal scale + efficiency: Full Hy4 770B open weights + WeMM-Video omni family under relatively open licenses (with commercial caveats).
- Agent-generated science and executable verification: alphaXiv experiment shows agents can produce volume research with self-audit; math formalization advances.
- Structured extraction and omni understanding: Clairic for schema filling, WeMM for audio-visual.
- Free/low-cost compute stable; managed + local stacks remain key. Always independently verify benchmarks, licenses, VRAM needs, and availability.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber/specialized models, access is often restricted. Community licenses may exclude regions or restrict commercial use.*
