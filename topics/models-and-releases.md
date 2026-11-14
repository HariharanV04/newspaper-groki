# Models & Releases

Living document. New entries go at the top. Older entries are refined or marked superseded rather than duplicated.

**Last refined:** 2026-11-14

---

## New / Stabilizing Infrastructure (Nov 13-14)

### llama.cpp / ggml v1.0.0 (Nov 13, 2026)
- **Type:** Stable major release of the core C/C++ local inference libraries (libllama + libggml).
- **Role:** Foundation for running open-weight multimodal LLMs on consumer to enterprise hardware via quantization and optimized backends. First formal semantic versioning promise: MAJOR for breaking public C API changes, MINOR for features/backends/models, PATCH for fixes. Removes 35 deprecated functions, promotes NextN speculative decoding API, adds FP8 KV caches, host-memory MoE expert cache, external PLE loading. New support for Kimi-K3.1-Pro, Ripple-65B-Preview, xing4_0, drama-3 TTS, MageVL-Cowork + Kimi vision. Hardened llama-server, redesigned web UI, /v1/audio/speech endpoint. Supports >150 architecture variants.
- **Status:** Released on GitHub + HF blog. Packaging via Docker, Debian, Homebrew, etc. Enables more reliable downstream apps and bindings.

### OpenAI Daybreak Red Team + Defense Factory (Nov 12, 2026)
- **Type:** Closed AI agent products for cybersecurity (under Daybreak program; uses specialized models including GPT-6 Cyber lineage).
- **Role:** Red Team: coordinated agents for web application penetration testing, vulnerability validation (scanners/bug bounties/disclosures), and patch verification in isolated environments with Guardian review. Defense Factory: agents investigate findings, trace through codebases, and draft patches + tests as PRs for human engineer review (integrates with Wiz, Snyk, Endor Labs, etc.).
- **Status:** Announced at Cyber at the Frontier. Red Team in early access; Defense Factory more broadly available. Pricing not yet public. Extends prior $1B cyber access pledge and specialized cyber models.

## Frontier / Flagship & Large Open

### Google Gemini 4 Hydrogen (Nov 12, 2026)
- **Type:** Closed fast agentic model (Gemini 4 series; adapted from Carbon).
- **Role:** Rapid execution across everyday coding and diverse agentic workflows. 1M unified input+output context. Thinking levels LOW/MEDIUM/HIGH (default)/XHIGH. Claims 2.5× faster than Gemini 3.8 Flash at default, stronger Terminal-Bench, fewer fabrications; competitive with / surpasses Argon on some independent indexes at higher thinking.
- **Status:** Generally available globally (Gemini API, AI Studio all tiers, Search, Gemini app, Antigravity for Pro/Ultra, business, Android Studio). $1.50 / $7.50 per M tokens. Replaces prior Flash role for many surfaces. Free tier available in AI Studio.

### Edge0-145B / Edge0-120B (Nov 12-13, 2026)
- **Type:** Open-weight latent MoE (145B total / ~10B active; 120B / ~8.6B active). Derived from Qwen3.8-Flash-Next, natively 4-bit trained. 48 layers, 512 experts, K=10, latent compression.
- **Role:** Local/laptop/single-GPU agentic coding and reasoning. High reported throughput on consumer NVIDIA (e.g. 100+ tok/s agent decode on 5090-class). Strong self-reported Terminal-Bench 2.1 (~86.5), DeepSWE, GPQA.
- **Status:** Weights on Hugging Face (Q3_K and NVFP4 variants). Runs via edge0-infer + edge0-strata (fork of Strata) on Linux/Windows with NVIDIA GPU + CUDA 13. Also supports Mac in some constrained configs. License: personal/research/internal OK; commercial/paid service requires separate agreement + underlying Qwen terms. Memory claims vary by source and quantization.

### MiniMax H3-Image (Nov 10-11, 2026; ongoing top trending)
- **Type:** Open-weight image generation/editing model (33.1B DiT based on MiniMax H3 architecture, without audio layers).
- **Role:** Native 4K / ~16MP (4096×4096 up to 6272×2688) text-to-image and multi-reference editing (up to 16 images) in under 10-16 seconds (6-step distilled sampling, no CFG). Strong prompt adherence. One checkpoint for T2I + editing.
- **Status:** Weights on Hugging Face (`MiniMaxAI/MiniMax-H3-Image`); community license (excludes EU, UK, South Korea, US). Also via MiniMax API, MiniMax Code, Hailuo AI (launch discounts). Native ComfyUI / Diffusers support. Rapidly trending on HF. Optional prompt expander available.

### PAN 2 (IFM / MBZUAI, Nov 10, 2026)
- **Type:** Open 29B world model (MMDiT diffusion backbone + frozen Qwen3.5-9B text encoder + Wan 2.2 VAE). Apache 2.0.
- **Role:** Action-conditioned video simulation of future world states (text description + optional starting image → up to ~20s video at 704×1248 / 24 fps). Supports simulative reasoning for agents (imagine outcomes before acting). Generative Latent Prediction architecture.
- **Status:** Weights, training and inference code released. Supported in Diffusers, vLLM, FastVideo, ComfyUI community nodes. Ranks highly among open models on Physics-IQ (vendor).

[... previous content continues with Baidu ERNIE, Qwen4-Max-Preview, Claude Fable 5.2, Gemini 4 Carbon, Muse Ember, LongCat-2.5, GPT-6 Cyber, Kimi K3.1 Pro, etc. as refined earlier ...]

*Note: Full historical entries remain below this refined top section. Older items (pre-Nov 12) are retained for continuity and marked as ongoing where still relevant.*
