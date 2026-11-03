# Current AI Briefing

**Last updated:** 2026-11-03

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24h (Nov 2-3)
- **Weight-Space Programming (MIT CSAIL, Nov 2)**: GPT-6 Astra demonstrated the ability to read and surgically edit neural network weights directly (no gradients, no training loops). In a public report, it modified ~0.016% of Qwen3.5-0.8B weights (131,072 entries), eliminating reasoning loops and raising MATH-500 from 7.9% to 48.1%, GSM8K from 13.8% to 67.1%, and IFEval from 21.0% to 62.3%. Full logs released. Also showed ability to identify trained behaviors from raw weights and write small policy networks from scratch.
- **Hydrogen-1.0 (Deep Principle, Nov 2)**: 753B-parameter open-weight scientific MoE (MIT license, ~40B active, 1M context). Post-trained from Z.ai GLM-5.3 on proprietary lab records, chemistry, materials science, and life sciences data + discovery trajectories. Self-reported 38.3% on FrontierScience-Research vs 33.3% for GPT-6 Astra. Weights on Hugging Face (gated) and ModelScope; quantized variants available. Not independently verified.
- **LongCat-2.5 (Meituan, Nov 2)**: Native multimodal 1.6T total / ~48B active MoE for long-horizon agentic tasks (coding, visual coding, 3D, full project builds). 1M context. Trained with large-scale agentic RL on long trajectories; optimized for Chinese domestic chips. API live (limited-time pricing ~$0.30/$1.20 per M tokens); GitHub/HF weights listed as coming soon. Strong self-reported scores on Terminal-Bench, BrowseComp, MCP Atlas, and related agent benchmarks (often competitive with Claude Opus 4.8/5 range).
- **Mistral Large 4 ("Le Chonk")**: Continued high traction. Open weights (1T total / ~52B active multimodal MoE) remain the top open model on Artificial Analysis Coding Agent Index; improved Terminal-Bench 4.0 to ~41%. Uses fewer tokens than peers for similar agentic coding results. HF activity strong; day-0 support in transformers/vLLM/llama.cpp.

### Ongoing traction & recent
- DeepSeek-V4.1-Flash-1017, Qwen3.8-27B (millions of downloads), LFM3 family, Nemotron series, LTX-2.5, Unlimited-OCR-2 continue as top HF activity.
- GLM 5.3 FlashX Legal listed on OpenRouter.
- Decision models (Drex Max, joey-1) and local coding agents (dsh-superagent) remain relevant.
- Gemini 4 Carbon and GPT-6 family models continue limited or API availability with strong vendor scores.

## Hugging Face & Ecosystem Updates
- Trending / high activity (Nov 2-3): mistralai/Mistral-Large-4-1T-A52B, deepseek-ai/DeepSeek-V4.1-Flash-1017, Qwen/Qwen3.8-27B, LiquidAI LFM3 variants, Lightricks/LTX-2.5, NVIDIA Nemotron models, Baidu Unlimited-OCR-2, and GGUF quantizations.
- New notable: Hydrogen-1.0 (deep-principle) gated release; community interest in weight-editing demos related to the MIT work.
- Ecosystem: Continued support in transformers, vLLM, TRL, Diffusers, llama.cpp, SGLang. FreeToken and local runtimes active for MoEs.

## Research (recent arXiv / HF Papers ~Nov 2-3 focus)
- **Weight-Space Programming** (MIT CSAIL): Standout result — frontier LLMs can inspect and directly edit weights of smaller models to fix failure modes and improve performance without traditional training. Broader experiments include identifying game policies from weights and writing networks from scratch.
- Efficiency: Latent Sparse Attention / subquadratic long-context methods; hierarchical attention variants; Muon-RT optimizer variants for self-distillation.
- Agents: Memory evaluation at point of use (MemUse), agent safety (AgentShield, MemHarmBench), long-horizon skill retrieval, recursive self-improvement harnesses.
- Other: StreamVibe-style video agents, scientific discovery models, causal world models.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (verified ~Nov 2-3 2026):**
- Google AI Studio / Gemini API: Free tier on Gemini 3.x Flash family and Gemma 4 variants (per-model limits; may train on prompts).
- Groq: Free plan with rate limits for open models including Qwen and others.
- NVIDIA NIM (build.nvidia.com): Free endpoints for Nemotron, DeepSeek Flash, GLM, Gemma, Muse, etc. (Developer Program key + phone verification).
- OpenRouter :free models, Cloudflare Workers AI (10k neurons/day), Requesty and other aggregators with card-free tiers.
- Hugging Face ZeroGPU (shared Blackwell for Spaces, short daily quota), Google Colab free tier, Kaggle Notebooks.
- Local: FreeToken (GPU+CPU+RAM pooling for large MoEs on consumer hardware), Ollama, llama.cpp, MLX, vLLM.
- Other: Modal/Lightning free credits (check current), various startup GPU grant programs.

**Hosting & tools:**
- Open weights of Mistral Large 4, Hydrogen-1.0, DeepSeek Flash, Qwen, LFM3, Nemotron available for self-hosting or free endpoints.
- Decision models and local coding agents for efficient agent loops.
- Diffusers/ComfyUI for generation (LTX-2.5, Pika H3 Flex, FLUX.3).
- Coding agents with free tiers (GitHub Copilot Free, etc.).

## Trending Themes
- Direct weight-space manipulation by frontier models (Weight-Space Programming) as a new editing/programming paradigm beyond gradients.
- Specialized open-weight scientific models (Hydrogen-1.0) post-trained on proprietary lab data.
- Large multimodal agentic MoEs from non-Western labs (LongCat-2.5, Mistral Large 4) emphasizing long-horizon coding and efficiency.
- Continued dominance of efficient open multimodal weights on HF with free API access.
- Local inference stacks and free compute tiers keeping frontier open models accessible to developers.
- Agent evaluation, memory, safety, and long-context efficiency research.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases.*
