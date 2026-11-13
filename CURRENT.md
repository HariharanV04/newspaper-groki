# Current AI Briefing

**Last updated:** 2026-11-13

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24-48h (Nov 12-13)
- **Google Gemini 4 Hydrogen** (Nov 12): Fast agentic model for everyday coding and workflows (replaces 3.8 Flash role). 1M unified input+output context window, thinking levels LOW/MEDIUM/HIGH (default)/XHIGH. Priced $1.50 input / $7.50 output per M tokens (flat across context). Available globally in Gemini API/AI Studio, Search, Gemini app, Antigravity (Pro/Ultra), Android Studio, business. Google claims 2.5× faster than prior Flash at default high, more than triples Terminal-Bench 4.1 scores, cuts fabricated claims >5×, surpasses Argon on Artificial Analysis Intelligence Index at high (51 vs 50) and higher at xhigh. Adapted from Carbon lineage. Knowledge cutoff ~March 2026.
- **Edge0-145B (and Edge0-120B)** (Nov 12-13): Open-weight latent MoE models (145B total / ~10.12B active per token; 120B / ~8.64B active). Derived from Qwen3.8-Flash-Next, trained natively at 4-bit. Designed for local/laptop/single NVIDIA GPU (Linux/Windows CUDA 13 via edge0-strata/edge0-infer). Reported speeds: 100+ tok/s agent decode on RTX 5090-class, high prefill; constrained memory tests (16 GiB VRAM + 20 GiB RAM) also shown. Strong self-reported Terminal-Bench 2.1 (~86.5), DeepSWE, GPQA-Diamond. Weights on HF (Q3_K / NVFP4 variants: Edge0/Edge0-145B-q3k etc.). License restricts full commercial use (personal/research/internal OK; paid service needs separate deal + Qwen terms). Memory footprint claims vary (peak ~29 GB in launch posts; model card constrained tests lower). Also 35B phone model previously.
- **MiniMax H3-Image** (ongoing, Nov 10+): Continues as top HF trending. Open-weight 33.1B DiT (H3 architecture) for native ~16MP/4K (4096×4096 up to wider) T2I + multi-reference editing (up to 16 images) in ~6 steps / under ~10-16s (no CFG). Community license (excludes US/EU/UK/South Korea etc.). Via HF, MiniMax API/Hailuo (launch discounts), ComfyUI/Diffusers native.
- **PAN 2** (IFM at MBZUAI, Nov 10): 29B open world model (Apache 2.0) for action-conditioned video simulation. Takes text (structured world-state) + optional image, outputs up to ~20s video at 704×1248 / 24 fps. Generative Latent Prediction architecture (LLM conceptual reasoner + MMDiT diffusion + Wan 2.2 VAE). For agent simulative planning. Weights/code on HF/GitHub; Diffusers/vLLM/ComfyUI support. Ranks well on Physics-IQ among open models (vendor).
- **Hugging Face Diffusers v0.43** (Nov 12): Integrates MiniMax-H3-Image, PAN 2, Kandinsky S2V 1.0, Pika H3 Flex, P-H3-Image modular pipelines. Attention backend fixes, dependency hardening.

### Ongoing traction & recent
- Anthropic Claude Whiteboards, Sheets, Data (beta/GA) + Meetings (Team/Enterprise beta for Google Meet): Collaborative artifacts and in-call context.
- NVIDIA Snapshot: Open-source Kubernetes GPU checkpoint/restore (CPU+GPU memory state). Restores initialized inference replicas (vLLM/SGLang/TRT-LLM) in 3.6–42.7s (8–36× vs cold start) across tested configs. Partners report large speedups (e.g. GLM-5.3 ~8 min → ~31s).
- Kimi K3.1 Pro, Ripple-65B-Preview, Arete-27B, LongCat-2.5, Mistral Large 4, Qwen3.8-27B family, uncensored DeepSeek variants, idol (image-to-3D), LTX-2.5 continue high HF activity.
- ERNIE 5.5 Flash Preview / Qwen4-Max-Preview / Gemini 4 Carbon / Claude Fable 5.2 remain relevant from prior days.

## Hugging Face & Ecosystem Updates
- Trending (as of Nov 13): MiniMaxAI/MiniMax-H3-Image (leader/rising fastest in multiple trackers), xtools-at/DeepSeek-V4-Pro-Qwen3.5-9B-UNCENSORED-heretic, NousResearch/Arete-27B, speridlabs/idol, Lightricks/LTX-2.5, Qwen/Qwen3.8-27B and Turbo/heretic GGUFs, ricursiveAI/Ripple-65B-Preview, moonshotai/Kimi-K3.1-Pro, ccore/Qwen3.5-4B-3D-Coder, Comfy-Org MiniMax-H3-Image variants.
- Ecosystem: Diffusers 0.43 day-0 support for new image/video/world models; Transformers ongoing; edge0 local inference stack; NVIDIA Snapshot for serving scale-out.

## Research (recent arXiv / HF Papers ~Nov 11-13 focus)
- Ongoing high volume in cs.AI: agent evaluation frameworks, evidence-linked memory for LLM agents, world models / generative latent prediction, efficiency (mixed-precision, early stopping in reasoning models), scientific discovery agents, safety/auditing of multimodal judges, robotics/computer-use agents.
- AlphaGenome 2 (DeepMind) continues traction for cell-type-specific variant effect prediction (nearly 2× causal recovery in some benchmarks; free non-commercial API).
- Themes: Local/efficient large MoEs, action-conditioned world simulation, agent reliability/memory, high-res open image gen, checkpoint/restore for inference scale.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (as of Nov 13 2026):**
- Kaggle: ~30 GPU hours/week (T4x2 or P100, 12h sessions).
- Google Colab free: limited GPU access / quota.
- Lightning AI: free GPU hours/credits + Studio.
- Hugging Face ZeroGPU: shared high-end GPU minutes/day for Spaces demos.
- Modal: $30 free compute/month + startup programs.
- NVIDIA NIM free endpoints, Groq, Google AI Studio (Gemini family including Hydrogen), OpenRouter free models, Cloudflare Workers AI (10k neurons/day), SambaNova free tiers.
- AMD Developer Cloud $100 MI300X credit (approved developers); various startup GPU/API credits (RunPod, Lambda, Google/AWS/Azure programs).
- Local: edge0 for large latent MoE on consumer NVIDIA, Ollama/llama.cpp (GGUF/FP8), vLLM/SGLang, ComfyUI/Diffusers for H3-Image/PAN 2/LTX, MLX. Strong for new open releases.

**Hosting & tools:**
- Open weights: Edge0-145B/120B (local NVIDIA), MiniMax-H3-Image (image), PAN 2 (world model), Kimi K3.1 Pro, Ripple-65B, Arete-27B, LongCat-2.5 available for self-host or endpoints (check licenses/VRAM).
- Coding agents: Claude Code, Cursor, Codex, Copilot, Antigravity, Cline dominant. Anthropic workspace expansion (Whiteboards/Sheets/Meetings).
- Inference serving: NVIDIA Snapshot for fast scale-out/restore; day-0 support for new models.
- Video/image/world: H3-Image native 4K, PAN 2 simulation, LTX-2.5, Cosmos/GR00T robotics.

## Trending Themes
- Local large-model breakthrough: Edge0-145B brings 100B+-class agentic performance to single consumer GPU / laptop with high throughput.
- Fast open image generation: MiniMax H3-Image dominates HF trending with practical native 4K + multi-ref editing.
- World models for agents: PAN 2 open Apache 2.0 action-conditioned video simulation for planning.
- Frontier speed/price: Gemini 4 Hydrogen as accessible fast agentic model; Carbon/Fable competition continues.
- Serving efficiency: NVIDIA Snapshot cuts cold starts from minutes to seconds for Kubernetes inference fleets.
- Accessible free/local compute and coding agents remain foundational; HF trending led by high-res image, local MoEs, 3D, and strong open models.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber/specialized models, access is often restricted. Community licenses may exclude regions or restrict commercial use.*
