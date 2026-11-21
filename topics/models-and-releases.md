# Models & Releases

Living document. New entries go at the top. Older entries are refined or marked superseded rather than duplicated.

**Last refined:** 2026-11-21

---

## New / Stabilizing Infrastructure (Nov 20-21)

### Thinking Machines Inkling 2 Mini (Nov 20, 2026)
- **Type:** Open Apache 2.0 looped MoE multimodal (~26.4B total / 3.4B active; research varloop option). Text+image in, text out, 1M context. ~20GB checkpoint.
- **Role:** High-capability local/edge model for agents, coding, chat, RAG. Leads open models <100B on several agent benches.
- **Status:** Weights on HF. Supports Transformers, llama.cpp, MLX, SGLang. Available on Tinker. Designed for 32GB+ unified memory devices.

### Tencent Hy4 full open weights (Nov 20, 2026)
- **Type:** Natively multimodal MoE flagship (770B total / 49B active + vision). 1M context, vision + computer use.
- **Role:** Long-horizon multimodal agentic work, coding, office, research. Now self-hostable.
- **Status:** Hy4, Hy4-FP8, base on HF/ModelScope/GitCode under Tencent Hy License 1.0 (commercial restrictions for large MaaS). Day-0 vLLM/SGLang. System Card with safety evals (cyber/bio). GGUF available.

### Tencent WeMM-Video family (Nov 20, 2026)
- **Type:** Omni-modal (text/image/audio/video → text). 2B/4B/9B dense + 35B-A3B MoE.
- **Role:** Joint audio-visual video understanding. Claimed open SOTA.
- **Status:** Apache 2.0 weights + quantized builds on HF. Technical report released.

### Cloudflare Clairic (Nov 20, 2026)
- **Type:** Open Apache 2.0 27B (on Qwen3.8-27B) + 9B flash for structured schema extraction from text/JSON/images.
- **Role:** High-accuracy structured data extraction, faster than OCR pipelines.
- **Status:** Weights on HF. Flash low-latency.

### NVIDIA Nemotron-Labs-Sigma (Nov 21, 2026)
- **Type:** 14 open continuous diffusion language model checkpoints.
- **Status:** Open weights released.

## Ongoing / Recent (Nov 17-19)

### Google Gemini 4 Neon (Nov 18, 2026)
- **Type:** Closed mid-tier Gemini 4 model (adapted from Carbon). Multimodal (text/image/video/audio/PDF), 1M context, thinking levels low/medium/high/xhigh.
- **Role:** Frontier-level intelligence for complex coding, knowledge work, and science at higher speed and lower cost than top-end models.
- **Status:** API $3/$15 per M tokens (cached $0.15). Live in Gemini API/AI Studio, Antigravity (Pro/Ultra), Gemini app (replaces Argon), GitHub Copilot. Strong AA Index (~61 xhigh), #1 Coding Agent Index, Vals, Terminal-Bench, science benches. No free tier. Knowledge cutoff ~March 2026.

### RadixArk DaisyRose-27B (Nov 18, 2026)
- **Type:** Open Apache 2.0 RL-tuned Qwen3.8-27B (BF16/FP8/NVFP4). 256K context, image input retained.
- **Role:** Efficient post-training for long-horizon agent tasks; large gains from small curated data + compute.
- **Status:** Weights on HF. Terminal-Bench 4.1 5.6% → 12.0%; gains on SWE-bench Pro, DeepSWE, IFBench, GPQA etc. Trained 18 days / 144 H200s on 1,200 tasks.

### Reson8 Rumble-2-Flash (Nov 18, 2026)
- **Type:** Open Apache 2.0 0.5B speech ASR, 40+ languages, auto detection.
- **Role:** High-efficiency multilingual ASR matching larger models on real call-center and Open ASR benches; very high throughput.
- **Status:** Weights on HF. Native Transformers/vLLM support. Practical for edge/deploy.

### OVHcloud Olala mini 7A1B (Nov 19, 2026)
- **Type:** Open Apache 2.0 hybrid Mamba-3/attention MoE (~6.8B / ~1B active), 32K context.
- **Role:** Compact reasoning model from European cloud provider.
- **Status:** Weights on HF (base/SFT/GGUF/MLX).

### Microsoft Aion 1.0 Instruct (Nov 18, 2026)
- **Type:** Open MIT 2.3B (32K, 8 languages).
- **Role:** Small language model; optimized version for Windows OS by early 2027.
- **Status:** Weights on HF.

### Phancy Phai-A1 (Nov 18, 2026)
- **Type:** Open (Apache) fast coding/agent model post-trained from Qwen, 1M context.
- **Role:** PC/Huawei Ascend runnable agentic coding.
- **Status:** Open weights released.

### Tencent Hy4 flash (open weights Nov 17-18, 2026)
- **Type:** Open multimodal MoE (220-224B total / 12B active, incl. Engram), 1M context.
- **Role:** Cost-efficient multimodal and long-context work; now self-hostable.
- **Status:** Weights (base/FP8) on HF/ModelScope under Tencent Hy License. Strongly trending. Prior ultra-cheap API ($0.07/$0.281).

*Note: Full historical entries remain below this refined top section. Older items are retained for continuity and marked as ongoing where still relevant. See git history for complete prior content.*
