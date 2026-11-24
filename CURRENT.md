# Current AI Briefing

**Last updated:** 2026-11-24

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24-48h (Nov 22-24)
- **Z.ai / Zhipu GLM-5.4** (Nov 23, 2026): First flagship Loop Transformer. Runs 28 layers of the GLM-5 base twice (shared weights) for deeper reasoning at ~750B scale, claimed to reach intelligence comparable to 2T-3T models. 1M context, native vision (up to high-res images/video), focused on "Generalized Coding" (code for video, games, 3D modeling, mechanical design, etc.). Available in GLM Coding Plan, ZCode, and Z.ai Chat (higher weekly quota for some users); per-token API and open weights planned after safety hardening. Reported gains on vulnerability finding (~47% more than GLM-5.3 in tests) and shorter outputs on some reasoning benches in ablations. Speeds up to ~200 tok/s off-peak. Risk noted: potential "marathon thinking" loops on hard prompts.
- **Thinking Machines / Hugging Face Inkling 2 Mini** (Nov 20, still heavily trending): Open Apache 2.0 looped MoE multimodal (~26.4B total / ~3.4B active; middle 12 of 24 layers run 3x, research variable-loop variant). Text+image in, 1M context, ~20GB mixed NVFP4/MXFP8 checkpoint for local use (32GB+ Macs, etc.). Supports Transformers, llama.cpp, MLX, SGLang, Ollama. Leads or matches open <100B models on multiple agentic/coding benches. Massive HF downloads on GGUF variants.
- **Ant Group / inclusionAI Ling-3.2-air** (Nov 23): Open MIT multimodal MoE (124B total / 5.5B active), 256K+ context (extendable), strong on document reasoning and workflows. Weights on HF.
- **Ant Group LingSante medical models** (Nov 23): Open MIT family from Afu health app. LingSante-3.1-flash (560B total / ~25B active hybrid-linear MoE, 1M context, clinical reasoning/tool-calling) and LingSante-3.1-air-VL (124B / 5.5B active multimodal for imaging, reports, assessments). On HF for local/research use.
- **China Telecom Xing4.1-Preview** (Nov 22): 285B total / ~17B active MoE with MLA + sparse attention, native 1M context, agentic coding focus. Apache 2.0 BF16 weights on HF + API.
- **Other notables**: MemTensor MemT-1.0-Pro (memory-native 554B/59B on Nemotron, open weights); OCRia-nano-1 (tiny 8.1M CPU document parser, modified Open RAIL); Clover-35B-A3B-Preview (diffusion LM, 35B/3B, high SWE scores claimed); Upstage Solar Mini 4.5 Preview (35B/3B MoE, 512K); ongoing GPT-6.2 Sol everyday-conversation rollout, Gemini 4 Neon, Hy4 variants, Qwen adapters.

### Hugging Face trending (as of Nov 24)
thinkingmachines/Inkling-2-Mini (#1) and unsloth/Inkling-2-Mini-GGUF (massive downloads), inworld/voice-isolator, harness-hub/Qwen3.8-27B-pi-adapted (agent LoRA), higurashi-ai/Haru-4B (audio), tencent/Hy4-flash, Lightricks/LTX-2.5, MiniMax-H3-Image, Qwen3.8-27B family. Strong activity on looped/efficient local models and agent adapters.

## Hugging Face & Ecosystem Updates
- Day-0/strong support continues for new open models (Inkling variants, Hy4, Ling family, medical models) across Transformers, vLLM, SGLang, Unsloth, llama.cpp, MLX.
- HF Daily Papers: MemOnce (scalable memory cutting cache 1313x and prefill 6.9x at 1M context), cmHC (manifold-constrained hyper-connections for residual stream stability), Clover diffusion LM technical report, non-penetrating world models, video foresight reasoning.
- Local/edge accessibility accelerating: Inkling Mini practical on consumer hardware; medical and small specialized models open under permissive licenses.

## Research (recent arXiv / HF Papers ~Nov 22-24 focus)
- **MemOnce**: Scalable LLM memory architecture using encoder-decoder on final hidden states + sparse attention; 1313× cache reduction and 6.9× prefill speedup at 1M context on Qwen-class models. Linear complexity for long-horizon tasks.
- Gemini 4 agent teams (DeepMind): Discovered and Lean-proved optimized quantum circuits with large compute reductions (e.g., arcsin routine ~290×, inertial confinement fusion ~11.8× in reported cases). Formal verification of agent-discovered algorithms.
- Anthropic Claude: Claimed Lean proof of Valiant’s VP ≠ VNP (open since 1979); not yet independently human-verified. Parallel mentions of AI-assisted Riemann Hypothesis progress.
- Other: Speculative decoding improvements (DICE), world model penetration benchmarks, video foresight self-distillation, medical MLLM visual values, agent swarm attempts on hard problems (e.g., P vs NP).
- Broader: Efficiency of looped/MoE architectures, memory systems for long context, agentic science and formal verification, multimodal medical and coding agents.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (as of Nov 24 2026):**
- **Kaggle Notebooks**: ~30 GPU hours/week on 2×T4 (sessions ≤12h). Most reliable free quota for experiments/fine-tuning. Phone verification.
- Google Colab free: T4 (16GB) when available, session/quota limits; paid unlocks L4/A100/etc.
- Hugging Face ZeroGPU: Short daily shared high-end GPU minutes for Gradio Spaces (PRO much more). Demo-oriented.
- Modal: $30 free credits/month on Starter.
- Cloudflare Workers AI, Groq free tier, Google AI Studio, OpenRouter free models, NVIDIA NIM free endpoints, Lightning AI free tier, E2B/Daytona sandboxes, SageMaker Studio Lab (limited hours).
- Cheap paid: Shadeform marketplace H100 from ~$2.73/hr; RunPod/Lambda/Nebius competitive H100 rates (~$3.8-4.5/hr). Startup/student GPU credit programs active.
- Local: llama.cpp, Unsloth GGUFs (Inkling, Qwen), MLX. Inkling 2 Mini practical on 32GB+ unified memory. Tools like gpu-free-serve for tunneling free notebook GPUs as OpenAI-compatible endpoints.

**Hosting & tools:**
- Open weights gaining: Inkling 2 Mini (local), Ling/LingSante (MIT medical/multimodal), Xing4.1, Hy4 family, Clover diffusion, DaisyRose agent post-training.
- Coding/agent tools: Anthropic Claude Ship (GitHub-integrated agents for review/PR/approvals); OpenAI Codex + Shirudo for agent-driven eBPF defenses; Cursor, Copilot, OpenHands, Antigravity, OpenCode.
- Inference: Strong day-0 support. Unsloth improvements for Inkling decoding; vLLM/SGLang/Transformers.
- Security tooling: Shirudo (OpenAI+Cisco open-source eBPF runtime) lets agents deploy signed temporary shields on running Linux systems without restarts while patches are rolled out (based on Tetragon; BSD license; pre-release with kernel/TPM requirements).

## Trending Themes
- Loop Transformer architectures: GLM-5.4 (large-scale flagship), Inkling 2 Mini (local), SenseNova-Loop and others — deeper reasoning via repeated shared-layer passes without proportional parameter growth.
- Open medical and specialized models: Ant LingSante family (MIT) for clinical reasoning and multimodal health; small CPU OCR and domain adapters.
- Agent-driven infrastructure security: Shirudo enables machine-speed temporary mitigations via eBPF while permanent patches land.
- Local/edge high-capability models + efficient memory: Inkling dominance on HF, MemOnce-style cache compression for long context.
- Free/low-cost compute stable (Kaggle primary); managed + local stacks remain key. Always independently verify benchmarks, licenses, VRAM needs, and availability.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber/specialized models, access is often restricted. Community licenses may exclude regions or restrict commercial use.*
