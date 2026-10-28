# Current AI Briefing

**Last updated:** 2026-10-28

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### Liquid AI LFM3 family (released Oct 27, 2026)
- Family of six open-weight ~2B-class models branched from LFM3-1.7B-Base (1.73B parameters).
- Covers text (LFM3-1.7B, 256K context), vision-language (LFM3-VL-2B with video), audio (LFM3-Audio-2B, speech in/out, 18 languages), omni (LFM3-Omni-2B), and two decision models (d1-2B, d1-Omni-2B returning typed/calibrated outputs).
- Tri-hybrid architecture (convolutions + sliding-window + global attention). Pretrained on 22T tokens. Fits ~1 GB at 4-bit. Fine-tunable on a single GPU. GGUF/MLX/ONNX/FP8/NVFP4 available.
- Liquid reports strong agentic gains vs prior LFM and competitive vs larger models on some benches (self-reported). Designed for local agents, specialized fine-tuning, edge deployment.
- Weights on Hugging Face (LiquidAI collection). Supports llama.cpp, MLX, vLLM, Transformers, etc.

### Google DeepMind Genie 4 (announced Oct 27, 2026)
- Next-generation real-time interactive world model with native audio (ambient, music, dialogue).
- Improved photorealism, physics, human characters, scene consistency up to ~2 minutes (double Genie 3). Real-time natural-language steering (change weather, camera, add elements).
- Integrates Gemini models (Omni for anchoring, Flash for reasoning/coherence).
- Research preview for trusted testers. Rolling out to Google AI Ultra subscribers in Project Genie and early Gemini API / AI Studio partners.

### OpenAI GPT-6.1 Terra (released Oct 26, 2026)
- Mid-tier model focused on visual reasoning, computer use, and everyday work tasks. 1.05M context.
- Pricing: $1 / $5 per million input/output tokens (half of prior Terra and Sol). Available in ChatGPT Work, Codex, and API (`gpt-6.1-terra`).
- OpenAI reports major gains on Terminal-Bench 4.0 (50.3% max effort vs 21.5% prior), Agents’ Last Exam, lower error rates, and 3x faster task completion than higher-end models.
- Positioned for high-volume agentic computer-use work.

### Ongoing / recent major
- Nanbeige4.3-33B (Oct 24-25): dense 33B Apache 2.0 agentic teacher remains highly relevant.
- Moonshot Kimi K3.1 Pro (open weights due Nov 4).
- Microsoft Agensh, Block Dessa, NVIDIA Nemotron Bolt E4B, Carbon-X, Recursive Flint, MiniMax M3.1 Flash continue strong.

## Hugging Face & Ecosystem Updates
- Trending / new: LiquidAI LFM3 collection (multiple modalities), ongoing Nanbeige, DeepSeek Flash, Flint, FLUX variants, MiniMax, Nemotron.
- Daily Papers continue heavy focus on agents, VLAs, world models, evaluation, and multimodal generation.
- Notable recent: Carbon-X DNA model still highlighted; various small specialized models (Telugu base, NPU-pretrained, etc.).

## Research (recent arXiv / HF Papers ~Oct 26-28)
- Strong continued emphasis on agents (user simulation, evolution frameworks, long-horizon), VLAs and robotics (force-reactive loco-manipulation, efficient humanoid training), world models, and evaluation of novelty/judging.
- Multimodal and generation advances (video agents, music, 3D).
- Safety and containment remain active topics (prior OpenAI red-team notes).
- Themes: specialized small multimodal models for edge (LFM3), real-time interactive simulation (Genie 4), cost-efficient agent computer use (Terra).

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (stable late Oct 2026):**
- Google Colab (limited T4), Kaggle Notebooks (~30h/week T4x2), Hugging Face ZeroGPU (shared high-end for Spaces, minutes/day)
- NVIDIA NIM free endpoints, Groq, Google AI Studio, OpenRouter, Cloudflare Workers AI
- Lightning/Modal free credits; NVIDIA Run:ai fully open-sourced (Apache 2.0) for self-hosted K8s GPU orchestration
- Startup grants; low-cost spots (RunPod/Vast.ai). Quantizations and single-GPU fine-tuning paths for new small models (LFM3).

**Hosting & tools:**
- Ollama/llama.cpp/Unsloth/MLX for local (LFM3 GGUF/MLX, Bolt E4B, Flint)
- vLLM/SGLang for larger models
- HF Hub/Spaces, Diffusers for image/video
- Agensh for multi-agent experiments
- Liquid API / Playground for LFM3

## Trending Themes
- Specialized small open multimodal models for local/edge agents and fine-tuning (LFM3 family)
- Real-time interactive world models with native audio (Genie 4)
- Cost-efficient mid-tier agent models for computer use (GPT-6.1 Terra)
- Dense mid-size agentic teachers (Nanbeige) and near-frontier open weights (Kimi)
- Multi-agent scaling (Agensh), speech-native models (Dessa), specialized scientific tools (Carbon-X)
- Efficient local agents and open inference stacks
- Free compute enabling broad experimentation

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor changelogs, arXiv, GitHub). Vendor scores are not independent.*
