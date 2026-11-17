# Models & Releases

Living document. New entries go at the top. Older entries are refined or marked superseded rather than duplicated.

**Last refined:** 2026-11-17

---

## New / Stabilizing Infrastructure (Nov 16-17)

### Alibaba Qwen4-Max (Nov 16, 2026)
- **Type:** Closed flagship MoE (~2.4T total / 71B active + N-gram embeddings), native vision, 1M context.
- **Role:** Long-horizon agentic work, coding, professional tools, 3D/scientific discovery. Efficiency-focused (claims significant token/cost reductions vs Qwen3.8-Max).
- **Status:** API live on QwenCloud ($1.50/$4.50); available in Qwen Studio, QwenWork, Qoder. Smaller Qwen4 open weights planned. 1M free quota for 90 days on some plans.

### Tencent Hy4 flash (Nov 16, 2026)
- **Type:** Closed low-cost multimodal MoE (224B total incl. Engram / 12B active), 1M context.
- **Role:** Cost-efficient multimodal and long-context work.
- **Status:** API live at $0.07 input / $0.281 output per M tokens on TokenHub. Weights and OpenRouter listing promised later. Available in WorkBuddy and Yuanbao.

### Meituan LongCat-Video-Avatar 1.6 (Nov 15, 2026)
- **Type:** Open-weight (MIT) audio-driven human video generation.
- **Role:** Improved lip sync, facial/body expressiveness, and long-video consistency (>10 min videos).
- **Status:** Weights + technical report on Hugging Face / ModelScope. Strong internal preference rankings.

### Meituan LongCat-2.5 (weights Nov 9; high coverage Nov 15-16)
- **Type:** Open-weight (MIT) multimodal MoE (1.6T total / ~48B active). Text/image/video input.
- **Role:** Long-horizon agentic coding and visual tasks. Trained on Chinese hardware (Huawei Ascend; no Nvidia).
- **Status:** Weights on Hugging Face. API with promotional pricing. Self-hosting requires large multi-accelerator setups. Strong self-reported Terminal-Bench scores.

## New / Stabilizing Infrastructure (Nov 14-15)

### Unsloth Dynamic V3.1 GGUFs for Qwen3.8-27B (Nov 11, 2026; high ongoing traction)
- **Type:** Improved quantized GGUF builds of the popular 27B dense vision-language model using Unsloth’s Dynamic V3.1 algorithm.
- **Role:** Highest-accuracy local inference for Qwen3.8-27B on consumer hardware. 5–10% average gains on Terminal Bench, DeepSWE, LiveCodeBench and other agentic/coding benchmarks vs prior UD3 and competing quants (GSQ-RCO, Exllama-v3) at similar sizes. Quants 2-bit to 6-bit updated; smallest builds run on ~12GB RAM.
- **Status:** Available on Hugging Face (`unsloth/Qwen3.8-27B-GGUF`). Also applied to DeepSeek-V4.1-Flash and Qwen3.8-Flash-Next. Documentation and benchmarks on Unsloth site. Compatible with llama.cpp and Unsloth Desktop.

### Weight-space programming advances (recent)
- **Type:** Technique for direct weight editing of small models without gradient-based training.
- **Role:** Lifts Qwen 3.5 0.8B from 7.4% to 58.7% on Math 500. Demonstrates continued progress in reading and modifying trained behaviors.
- **Status:** Weights and details shared via HF posts and related research. Builds on earlier MIT CSAIL work.

### BananaMind/BETU-SLM-Leaderboard (recent)
- **Type:** Community leaderboard focused on small language models.
- **Role:** Ranks models by Overall Index (weighted mix of Hellaswag, ARC Easy, PIQA, Arithmark 3, Tiny Theory of Mind, BananaMind Base Bench). Simple one-command addition of custom models.
- **Status:** Released and active.

## Frontier / Flagship & Large Open

### Google Gemini 4 Hydrogen (Nov 12, 2026)
- **Type:** Closed fast agentic model (Gemini 4 series; adapted from Carbon).
- **Role:** Rapid execution across everyday coding and diverse agentic workflows. 1M unified input+output context. Thinking levels LOW/MEDIUM/HIGH (default)/XHIGH. Claims 2.5× faster than Gemini 3.8 Flash at default, stronger Terminal-Bench, fewer fabrications; competitive with / surpasses Argon on some independent indexes at higher thinking.
- **Status:** Generally available globally (Gemini API, AI Studio all tiers, Search, Gemini app, Antigravity for Pro/Ultra, business, Android Studio). $1.50 / $7.50 per M tokens. Replaces prior Flash role for many surfaces. Free tier available in AI Studio.

### Inkling 2 Small (weights Nov 12, 2026)
- **Type:** Open-weight multimodal MoE (594B total / 17B active). Apache 2.0.
- **Role:** Agentic coding, vision, knowledge work, and reasoning. Strong open rankings in Agent Arena and Code Arena.
- **Status:** Weights live on Hugging Face. Day-0 support in vLLM, SGLang, Unsloth. API available via multiple providers.

### MiniMax H3-Image (Nov 10-11, 2026; ongoing top trending)
- **Type:** Open-weight image generation/editing model (33.1B DiT based on MiniMax H3 architecture, without audio layers).
- **Role:** Native 4K / ~16MP (4096×4096 up to 6272×2688) text-to-image and multi-reference editing (up to 16 images) in under 10-16 seconds (6-step distilled sampling, no CFG). Strong prompt adherence. One checkpoint for T2I + editing.
- **Status:** Weights on Hugging Face (`MiniMaxAI/MiniMax-H3-Image`); community license (excludes EU, UK, South Korea, US). Also via MiniMax API, MiniMax Code, Hailuo AI (launch discounts). Native ComfyUI / Diffusers support. Rapidly trending on HF. Optional prompt expander available.

*Note: Full historical entries remain below this refined top section. Older items (pre-Nov 12) are retained for continuity and marked as ongoing where still relevant.*
