# Current AI Briefing

**Last updated:** 2026-10-29

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### Google DeepMind Gemini 4 Carbon (announced Oct 28, 2026)
- Next frontier model, successor to Gemini 4 Argon. Google’s strongest to date with SOTA cybersecurity and long-horizon agentic capabilities.
- Tops Artificial Analysis Intelligence Index v5.0 at 59 (Argon was 50; ahead of Claude Opus 5.5 at 58, GPT-6 Astra at 57). Strong leads on SEC-bench Pro (88.2% vulnerability finding), ExploitGym (54.8%), CWE-bench (71.0% patching). Gains in coding agents, Terminal-Bench, GraphWalks, secure code generation (2x internal uplift), and prompt injection resistance (0% attack success).
- Built for multi-day autonomous workflows (bug root-causing, large codebase patching). Introductory pricing matches Argon: $2 / $10 per million input/output tokens (cached 95% off); later $4 / $20. No open weights.
- Limited access starts with cyber defenders under Fairwind Program this week; broader developer/business/consumer rollout later after feedback and guardrails. Engaged in US government pre-release testing.

### Google DeepMind Genie 4 (announced Oct 27, 2026)
- Next-generation real-time interactive world model with native audio (ambient, music, dialogue).
- Improved photorealism, physics, human characters, scene consistency up to ~2 minutes (double Genie 3). Real-time natural-language steering (change weather, camera, add elements).
- Integrates Gemini models (Omni for anchoring, Flash for reasoning/coherence).
- Research preview for trusted testers. Rolling out to Google AI Ultra subscribers in Project Genie and early Gemini API / AI Studio partners.

### Liquid AI LFM3 family (released Oct 27, 2026)
- Family of six open-weight ~2B-class models branched from LFM3-1.7B-Base (1.73B parameters).
- Covers text (LFM3-1.7B, 256K context), vision-language (LFM3-VL-2B with video), audio (LFM3-Audio-2B, speech in/out, 18 languages), omni (LFM3-Omni-2B), and two decision models (d1-2B, d1-Omni-2B returning typed/calibrated outputs).
- Tri-hybrid architecture (convolutions + sliding-window + global attention). Pretrained on 22T tokens. Fits ~1 GB at 4-bit. Fine-tunable on a single GPU. GGUF/MLX/ONNX/FP8/NVFP4 available.
- Liquid reports strong agentic gains vs prior LFM and competitive vs larger models on some benches (self-reported). Designed for local agents, specialized fine-tuning, edge deployment.
- Weights on Hugging Face (LiquidAI collection). Supports llama.cpp, MLX, vLLM, Transformers, etc.

### Other recent (past ~48h)
- Calix Communications Language Model released on HF (Oct 27): specialized telecom/comms model; plans for Calix Gems specialists in 2027.
- Cisco open-sourced Project Quarry (Oct 28): AI agent behavior detection engine for flagging risky sequences across sessions.
- Ongoing: Nanbeige4.3-33B, GPT-6.1 Terra (Oct 26), Recursive Flint, Carbon-X, MiniMax M3.1 Flash, Nemotron series.

## Hugging Face & Ecosystem Updates
- Trending / new: LiquidAI LFM3 collection (multiple modalities), DeepSeek-V4.1-Flash variants (high downloads), Nanbeige4.3-33B, Flint, FLUX.3 Image Klein, Unlimited-OCR-2 (Oct 26), Qwen3.5-4B-3D-Coder (Oct 25), Nemotron Transcribe, Carbon-X.
- HF blog (recent): Promptable Speech Recognition (Nemotron 3.5 Transcribe + Granary), Novelty Benchmarks (Ai2 on LLM research novelty judgments), LFM3 multimodal toolkit, DecisionFormer for structured decisions.
- Diffusers 0.42 with FLUX.3 Image Klein (layout control, reference editing), Transformers updates including EmbeddingGemma 2, Nemotron diarization.
- Daily Papers continue heavy focus on agents, VLAs, world models, evaluation, and multimodal generation.

## Research (recent arXiv / HF Papers ~Oct 27-29)
- Strong continued emphasis on agents (helpful agent problem / spontaneous cooperation, co-evolving rubrics, long-horizon), evaluation (novelty benchmarks, math proof verification with LLMs), RAG/ontology grounding, efficiency (KV cache, batching optimizers like GEPA), VLAs and robotics.
- Multimodal and generation advances; world models (Genie 4).
- Safety and containment remain active (agent risks, prompt injection).
- Themes: specialized small multimodal models for edge (LFM3), real-time interactive simulation (Genie 4), frontier long-horizon + cybersecurity (Carbon), cost-efficient agent computer use (Terra).

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (stable late Oct 2026):**
- Google Colab (limited T4), Kaggle Notebooks (~30h/week T4x2), Hugging Face ZeroGPU (shared high-end for Spaces, minutes/day)
- NVIDIA NIM free endpoints, Groq, Google AI Studio, OpenRouter free models, Cloudflare Workers AI
- Lightning/Modal free credits; NVIDIA Run:ai fully open-sourced (Apache 2.0) for self-hosted K8s GPU orchestration
- Startup grants; low-cost spots (RunPod/Vast.ai/Lium). Quantizations and single-GPU fine-tuning paths for new small models (LFM3).
- FreeInference.dev tracks 107 free LLM models across 36 providers (updated Oct 28).

**Hosting & tools:**
- Ollama/llama.cpp/Unsloth/MLX for local (LFM3 GGUF/MLX, Bolt E4B, Flint)
- vLLM/SGLang for larger models
- HF Hub/Spaces, Diffusers for image/video (FLUX.3)
- Agensh for multi-agent experiments
- Liquid API / Playground for LFM3
- Cisco Quarry for agent monitoring

## Trending Themes
- Frontier models emphasizing cybersecurity defense and multi-day long-horizon agentic work (Gemini 4 Carbon)
- Specialized small open multimodal models for local/edge agents and fine-tuning (LFM3 family)
- Real-time interactive world models with native audio (Genie 4)
- Cost-efficient mid-tier agent models for computer use (GPT-6.1 Terra)
- Dense mid-size agentic teachers (Nanbeige) and near-frontier open weights (Kimi)
- Multi-agent scaling (Agensh), speech-native models (Dessa), specialized scientific tools (Carbon-X)
- Efficient local agents, open inference stacks, and free compute enabling broad experimentation
- Agent safety, behavior detection, and evaluation reliability

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor changelogs, arXiv, GitHub). Vendor scores are not independent.*
