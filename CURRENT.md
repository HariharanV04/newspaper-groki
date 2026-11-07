# Current AI Briefing

**Last updated:** 2026-11-07

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24h (Nov 6-7)
- **Protegrity-PII**: Open-weights 278M-parameter token-level encoder (XLM-RoBERTa) for PII detection/classification across 69 entity types (beyond names/contacts to accounts, health, credentials, biometrics, etc.). On public PII-SCOPE benchmark: 0.910 typed recall at 0.902 precision, outperforming AWS Comprehend, Microsoft Presidio, OpenAI Privacy Filter. Processes 1M characters in 0.49s (~$0.0005) on single RTX 6000 Blackwell. Self-hosted for AI pipelines; technical report on arXiv; weights on HF.
- **Nous Research Arete-27B**: Post-trained (SFT ~52.8M tokens) Qwen3.8-27B to reinforce Western values / reduce state-aligned responses. Propaganda rate on 803-prompt eval dropped from 22% (base) to ~1% (matching Western models); fact mean improved 2.32 → 2.98/5. No significant capability regression on Hermes Bench or Terminal-Bench-2.1. Vision encoder frozen; weights, eval, training data public on HF under Apache 2.0.
- **Kakao Kanana-2-v-decide**: 3.67B multimodal decision model (on Kanana-2-v-3b) returning probabilities over choices/yes-no/scores (not free text). Accepts text/JSON/chat + up to 10 images (20k token context). Open weights under Kanana Open License on HF.
- **Kimi K3.1 Pro (Moonshot)**: Continues dominating HF trending (top model). 2.8T total / 104B active multimodal MoE, 1M context, MXFP4 (~1.56TB). NVIDIA free API endpoint available (build.nvidia.com, OpenAI-compatible, rate-limited). Strong agentic/coding performance.
- **Ripple-65B Preview (Ricursive)**: Dense 65B Apache 2.0 remains of interest for efficient agentic coding; self-reported strong Terminal-Bench 2.1.

### Ongoing traction & recent
- Mistral Large 4 high activity as efficient 1T open multimodal MoE.
- HF trending: moonshotai/Kimi-K3.1-Pro leading, LTX-2.5, Qwen3.8-27B, Nemotron Transcribe, Mistral Large 4, Ripple-65B, DeepSeek variants.
- Other: ERNIE-5.5-Flash-Base, Ling models, quantized GGUFs circulating.

## Hugging Face & Ecosystem Updates
- Trending / high activity: Kimi-K3.1-Pro (massive), Lightricks/LTX-2.5 (image-to-video), Qwen/Qwen3.8-27B, nvidia/Nemotron Transcribe, mistralai/Mistral-Large-4, ricursiveAI/Ripple-65B-Preview, various Qwen 3D-Coder and DeepSeek Flash GGUFs.
- Blog (Nov 6): Harness-Specific LoRA Adapters for training compact policies inside coding-agent runtimes (with safeguards); accent-specific private speech for Open ASR Leaderboard (Egyptian/Nigerian English); SuperCLUE split leaders insight for workload-specific evals; Phonon practical framework for on-device TTS.
- Ecosystem: Transformers 5.22.2 (hardened Jinja sandboxing + NCCL device ID fix); TRL 1.17 continues enabling LoRA on large models (e.g., Mistral Large 4 on single 8×B300); Diffusers security patches.

## Research (recent arXiv / HF Papers ~Nov 5-7 focus)
- **SwarmEvolve** (arXiv:2611.08483, Brown): Latent agent swarms for evolutionary discovery/optimization. Hundreds of low-cost agents reason in latent space (KV-cache sharing, no text decoding), novelty filtering via hidden states. On 21 math/scientific computing problems: highest average score, reaches SOTA baselines' 60-min scores in median 3-8 min. With Qwen3-8B improves on AlphaEvolve (frontier LLM) solutions on several problems. Fast, low-cost program search.
- **Scientist World** (arXiv:2611.08478): Pipeline converting papers into executable research environments/baselines for AI-Scientists. First 1,000 verified environments released. Frontier AI-Scientists surpassed human reported results 74% of the time; ~6,400 hours of traces; +158% ideation boost for small model matching frontier.
- Other: SAVeR² reasoning-based safety alignment via verifiable rewards; ARMs adaptive red-teaming for multimodal; ReproBridge for ML reproducibility; various agent safety, evaluation, efficiency papers.
- Themes: Agent swarms/latent reasoning for science, runnable research worlds, safety/alignment for reasoning models, evaluation frameworks.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (as of Nov 7 2026):**
- Kaggle: ~30 GPU hours/week (T4x2 or P100, 12h sessions).
- Google Colab free: limited GPU access, 12h max.
- Lightning AI: credits (~75h T4 or similar).
- Hugging Face ZeroGPU: shared RTX Pro 6000 Blackwell, ~5 min/day for Spaces demos.
- Modal: $30 free compute/month + startup credits (up to higher).
- NVIDIA NIM free endpoints (including Kimi K3.1 Pro), Groq, Google AI Studio, OpenRouter free models, Cloudflare Workers AI.
- Local: Ollama, llama.cpp (incl. FP8/GGUF), vLLM/SGLang, MLX, FreeToken for MoE pooling.
- Startup/research credits: NVIDIA Inception, Modal, Nebius, cloud trials (GCP/Azure).

**Hosting & tools:**
- Open weights: Kimi K3.1 Pro (heavy), Arete-27B (easy 27B), Protegrity-PII (tiny), Ripple-65B, Mistral Large 4 available for self-host or endpoints.
- Coding agents trending: Claude Code (high merge rates), Cursor, OpenAI Codex, GitHub Copilot, Google Antigravity, Cline (open), Devin.
- Inference: Day-0 support in Transformers/vLLM/SGLang; TRL for fine-tuning large models.
- Video/image: LTX-2.5, Flux.3, Pika H3 Flex, Gemini Omni.

## Trending Themes
- Open-weight giants (Kimi K3.1 Pro) + targeted alignment fine-tunes (Arete-27B de-biasing Chinese base models).
- Lightweight specialized models (Protegrity-PII for privacy in AI pipelines).
- Agent research advancing: latent swarms for discovery (SwarmEvolve), runnable scientific environments (Scientist World).
- Accessible free/local compute and coding agents democratizing capabilities.
- HF ecosystem maturing with security patches, LoRA for 1T models, decision models.
- Evaluation focus: workload-specific, accent coverage, safety for reasoning/agents.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber/specialized models, access is often restricted.*
