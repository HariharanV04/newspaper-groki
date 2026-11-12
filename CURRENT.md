# Current AI Briefing

**Last updated:** 2026-11-12

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24-48h (Nov 10-12)
- **MiniMax H3-Image** (Nov 10-11): Open-weight image model (33.1B DiT on H3 architecture) for native 4K (4096×4096 / ~16MP) text-to-image and multi-reference editing (up to 16 images) in under 10 seconds (6-step distilled, no CFG). Strong prompt adherence. Weights on Hugging Face (`MiniMaxAI/MiniMax-H3-Image`); community license excludes EU/UK/South Korea/US. Also via MiniMax API / Hailuo (50% off 4K during launch). Rapidly trending on HF. Native ComfyUI support.
- **Baidu ERNIE 5.5 Flash Preview** (Nov 11): First post-trained model on ERNIE 5.5 Flash Base. 280B total / 14B active MoE, 1M-token context, >200 tokens/s decoding. Strong at coding, 3D modeling (Blender/CAD), knowledge work, content creation. API live on Qianfan (ernie-5.5-flash-preview); weights to be open-sourced under Apache 2.0 by Nov 25. Intermediate checkpoint.
- **Alibaba Qwen4-Max-Preview** (Nov 11): Next-generation flagship multimodal (text + image + video input), 1M context, up to 393K output (shared with reasoning), reasoning on by default (low/medium/xhigh), tool calling, web search, structured outputs. Compatible with OpenAI and Anthropic APIs. Available only via Alibaba Token Plan (preview window Nov 11–25 UTC+8); no weights, no public benchmarks or per-token price yet. Early access also in Qwen apps.
- **Google DeepMind AlphaGenome 2** (Nov 11): Next-gen DNA sequence model predicting how variants affect specific human cell types (trained on 100M+ single-cell profiles across 68 tissues). Identifies nearly 2x as many causal variants and directional gene effects vs prior (e.g., 30% vs 16% causal on TenK10K immune cells). Free for non-commercial research via AlphaGenome API; commercial in private preview. Weights upon final publication.
- **Google Gemini 4 Carbon** (GA Nov 10, ongoing): Strongest Gemini 4 model. Intro $2/$10 per M tokens through Nov 30 (then $4/$20). 1M context. Strong long-horizon agentic/cybersecurity. Competitive with Claude Fable 5.2; cheaper. AlphaProof Code verified Signal protocol properties on real machine code.
- **Anthropic Claude Fable 5.2 & Mythos 5.2** (Nov 9, ongoing traction): ~30% faster, $8/$40. Tops AA Intelligence Index (65). Strong coding/science; multi-agent formal math (Fermat in 30h), electronics design, physics. Mythos gated.
- **Meituan LongCat-2.5** (full MIT weights Nov 9): 1.6T multimodal MoE / ~48B active. Ongoing relevance for long-horizon agentic coding/visual tasks.
- **Meta Muse Ember** (Nov 9): Small multimodal agent model ($0.10/$0.50) for tool calls, routing, extraction.

### Ongoing traction & recent
- Kimi K3.1 Pro (2.8T multimodal MoE) still high HF activity.
- Trending HF: MiniMax-H3-Image (rising to #1 in some trackers), uncensored DeepSeek variants (e.g. DeepSeek-V4-Pro-Qwen3.5-9B-UNCENSORED-heretic), speridlabs/idol (image-to-3D), NousResearch/Arete-27B (rising), Lightricks/LTX-2.5, ricursiveAI/Ripple-65B-Preview, Qwen3.8-27B and variants.
- Ripple-65B, Mistral Large 4, various 3D-Coder and agent GGUFs continue.
- NVIDIA GR00T 2 robotics world-action model; Cosmos 3.

## Hugging Face & Ecosystem Updates
- Trending (as of Nov 12): MiniMaxAI/MiniMax-H3-Image (fastest rising, high likes/downloads), xtools-at/DeepSeek-V4-Pro-Qwen3.5-9B-UNCENSORED-heretic, speridlabs/idol, NousResearch/Arete-27B, Lightricks/LTX-2.5, moonshotai/Kimi-K3.1-Pro, ricursiveAI/Ripple-65B-Preview, Qwen/Qwen3.8-27B, ccore/Qwen3.5-4B-3D-Coder, DavidAU uncensored Turbo GGUFs, baidu/ERNIE-5.5-Flash-Base.
- Recent: MiniMax H3-Image day-0 ComfyUI; ERNIE base and preview; continued Transformers/vLLM/SGLang support.
- Ecosystem: Price competition intensifying; open image/video stacks maturing (H3-Image, LTX-2.5).

## Research (recent arXiv / HF Papers ~Nov 10-12 focus)
- AlphaGenome 2 (DeepMind): Cell-type-aware DNA variant effect prediction; nearly doubles causal variant recovery on single-cell immune benchmarks; expression conditioning from user scRNA-seq without retraining. Free non-commercial API.
- Contrastive Discovery: Open-ended scientific discovery over competing explanations (LLM agents; better resolution of questions).
- MiniMax H3-Image technical details (native 16MP, 6-step).
- Agents: ReTrace (distilling tool-using agents into planner-free workflows), Evidence-Linked Memory (reduces memory-induced degradation), Infrathon (long-horizon AI infra optimization), World In-Context Learning for Agentic Robot Manipulation.
- Other: TorchCurves (differentiable parametric curves), medical image segmentation foundation vs task-specific, Tree-Ising weight-space repairs, few-step streaming video generation.
- Themes: Cell-specific genomics models, efficient high-res image gen, agent distillation/memory/reliability, scientific discovery agents.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (as of Nov 12 2026):**
- Kaggle: ~30 GPU hours/week (T4x2 or P100, 12h sessions).
- Google Colab free: limited GPU access, session limits.
- Lightning AI: up to ~30 credits (~50+ GPU hours on T4) + free Studio.
- Hugging Face ZeroGPU: shared RTX Pro 6000 Blackwell, ~5 min/day for Spaces demos.
- Modal: $30 free compute/month + startup credits.
- NVIDIA NIM free endpoints, Groq, Google AI Studio (Flash family), OpenRouter free models, Cloudflare Workers AI (10k neurons/day), SambaNova free until card linked.
- Notable: AMD Developer Cloud $100 credit on MI300X (approved); IteraCompute free Auto route (up to 30M tokens/month); various startup MaaS credits. Tiers remain stable.
- Local: Ollama, llama.cpp (FP8/GGUF), vLLM/SGLang, MLX, FreeToken for MoE pooling. Strong for new open models like H3-Image (quantized Comfy), Kimi, Ripple, Arete.

**Hosting & tools:**
- Open weights: MiniMax-H3-Image (community license, high-res image), LongCat-2.5 (MIT), Kimi K3.1 Pro, Ripple-65B, Mistral Large 4, Arete-27B available for self-host or endpoints. ERNIE weights upcoming.
- Coding agents: Claude Code, Cursor, Codex, Copilot, Antigravity, Cline remain dominant. Anthropic workspace (Whiteboards/Sheets/Data) expanding.
- Inference: Day-0 support for new releases; price competition (Carbon intro $2/$10, Qwen preview, ERNIE) lowering barriers. Open image stacks via ComfyUI/Diffusers.
- Video/image: MiniMax-H3-Image (native 4K), LTX-2.5, GR00T 2 / Cosmos for robotics.

## Trending Themes
- Rapid open image generation scaling: MiniMax H3-Image brings practical native 4K in <10s with open weights and multi-ref editing, rising to top of HF trending.
- Chinese flagships accelerating previews: ERNIE 5.5 Flash Preview (strong coding/3D, weights soon) and Qwen4-Max-Preview (multimodal 1M-ctx, limited Token Plan access) join the open/closed race.
- Genomics and specialized scientific models: AlphaGenome 2 doubles variant detection at cell-type resolution; free research access.
- Frontier price war continues: Carbon intro pricing undercuts Fable while remaining competitive; open weights (Kimi, LongCat, H3-Image) pressure proprietary.
- Agent capabilities and reliability: distillation, memory, long-horizon infra, formal verification ongoing. Robotics world-action models active.
- Accessible free/local compute and coding agents remain foundational; HF trending dominated by high-res image, uncensored variants, 3D, and strong open MoEs.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber/specialized models, access is often restricted. Community licenses may exclude regions.*
