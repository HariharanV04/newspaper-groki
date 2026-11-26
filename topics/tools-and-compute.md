# Tools & Compute

Living reference for free/low-cost GPUs, hosting, inference stacks, and developer tooling. Quotas and offerings change; update entries in place.

**Last refined:** 2026-11-26

---

## Free / Low-Cost GPU Access

| Provider | What you get | Notes / Limits |
|----------|--------------|----------------|
| Google Colab (free) | Hosted notebook, limited T4 (16GB) | Session limits (~12h); quota fluctuates; signed-out sees CPU/T4/v5e TPU |
| Kaggle Notebooks | 2×T4, ~30h/week (sometimes higher) | Phone verification; sessions ≤12h GPU; best reliable free quota for experiments |
| Hugging Face ZeroGPU | Shared RTX Pro 6000 Blackwell for Gradio Spaces | Short daily quota (5 min free); demo-oriented |
| NVIDIA NIM / build.nvidia.com | Free endpoints for many open models (Nemotron, DeepSeek-V4.1-Flash, GLM, Muse, Gemma, etc.) | OpenAI-compatible; NVIDIA Developer Program key (phone verification in supported countries). Rate limits vary. |
| Groq free tier | Fast inference on supported models (gpt-oss, Qwen3.8-27B, etc.) | Rate limits (e.g. 30 RPM / 1k RPD for coding models); no card |
| Google AI Studio / Gemini free | Flash/Hydrogen models (Gemini family + Omni), Gemma 4 | May train on prompts; usage per model; no card for free tier. Hydrogen available. |
| OpenRouter free | Limited free models / daily requests (Nemotron, Gemma, Inkling, Ling-3.2-flash 1M free, etc.) | Card-free options; ~50-1000 requests/day depending on plan |
| Cloudflare Workers AI | 10k neurons/day | Edge inference |
| SambaNova Cloud | Free use of hosted open models until payment method linked | Rate limits apply |
| Requesty / AIHubMix / other aggregators | Free model routes | Card-free free plans with daily quotas |
| Modal | $30 free compute credits/month | Starter plan, no monthly fee, GPU concurrency; startup programs available |
| Lightning AI | Free monthly compute / studios | Check current balances (e.g. up to ~30 credits / ~50 GPU hours on T4 + free Studio) |
| Daytona / E2B | $200 / $100 free compute for new accounts | Sandboxes for AI agents; no card |
| AMD Developer Cloud | $100 complimentary credit on Instinct MI300X | Approved developers via AI Developer Program |
| IteraCompute / others | Free token routes (e.g. up to 30M tokens/month Auto on open models) | No card for some; rate limited |
| NVIDIA Run:ai (open-sourced) | Full GPU orchestration (Apache 2.0) | Self-host; supply own K8s/GPUs |
| Startup programs | Credit grants | Vary (e.g. Inference.net up to $10k, Hostkey GPU grants, Novita, Google/AWS/Microsoft, GMI Cloud, fal, Together AI, Baseten, etc.) |
| RunPod / Vast.ai / Lambda / Nebius | Cheap spot / on-demand GPUs | H100 ~$3.8-4.5/hr typical; Shadeform marketplace from ~$2.73/hr H100 |
| **Together AI Preemptible** | Same NVIDIA GPUs as on-demand at flat 50% rate | Interruptible; 5-min drain/SIGTERM for checkpoint; auto-refill; sub-hourly billing. For training/batch/sweeps. K8s/Slurm. |
| Leafcloud (emerging) | Free Blackwell slices (waitlist) | 50h/month planned for RTX PRO 6000 slices |
| SageMaker Studio Lab | Limited GPU hours | ~4h/day approved accounts |
| ModelScope / Baidu AI Studio / Paperspace Gradient | Additional free quotas / public GPU notebooks | Check current daily/one-time limits |

## Hosting & Serving

- **Together AI Preemptible Compute** (Nov 24-25, 2026): GA on GPU Clusters. Flat 50% of on-demand for same hardware. 5-minute drain window, automatic capacity refill. Sub-hourly metering. Ideal for checkpointed training, evals, batch inference.
- **Shirudo** (OpenAI + Cisco, Nov 23, 2026): Open-source (BSD 2-Clause; BPF dual BSD/GPL) Linux runtime based on eBPF/Tetragon. Lets AI agents generate and deploy cryptographically signed temporary "shields" that block vulnerable code paths on running systems without restarts while permanent patches are tested/rolled out. Pre-release; requires special kernel + TPM 2.0. GitHub: shirudo-dev/shirudo. Demonstrated on Java4Shell-style exploits via Codex-generated shields.
- **Claude Ship** (Anthropic, Nov 23): Suite of GitHub-integrated agents (Code Review, PR Steward, Claude Approvals) for automated routine PR review, patching, and approval based on repo policies.
- **GLM-5.4**: Hosted in Z.ai Coding Plan / ZCode / Chat. API and weights after safety.
- **ERNIE 5.5 Flash Preview**: Open Apache 2.0 on HF. Day-0 vLLM/SGLang plugin. FP8/FP4 options + speculative decoding.
- **Inkling 2 Mini**: Open Apache 2.0 on HF (~20GB). Day-0 support in Transformers, vLLM, SGLang, Unsloth, llama.cpp, MLX, Ollama. Practical local on 32GB+ unified memory. Heavy GGUF activity. Still #1 trending.
- **Ternary Bonsai 2.5 27B**: Open GGUF ternary (~5.9GB). llama.cpp / MLX. Optimized for agents.
- **Ling / LingSante**: Open MIT weights on HF for multimodal and medical models.
- **Hy-MT3 / SenseNova U1.6**: Open Apache translation and self-correcting image models on HF.
- **Qwen4-Max** — Closed flagship. API on QwenCloud ($1.50/$4.50). Smaller open weights planned.
- **LongCat-2.5** — Full MIT weights on HF (1.6T MoE / ~48B active multimodal). Serve with vLLM/SGLang once recipes mature; large multi-node/accelerator needs. API available.
- **MiniMax H3-Image** — Open weights on HF for native 4K T2I + multi-ref editing. ComfyUI native; quantized options emerging. Community license (regional exclusions). API also available.
- **Unsloth Dynamic V3.1 GGUFs** — Highest-accuracy local builds for Qwen3.8-27B (and related) on 12GB+ RAM via llama.cpp / Unsloth Desktop. Improvements for Inkling decoding.
- **Inkling 2 Small** — Open Apache 2.0 weights on HF (594B/17B MoE). Day-0 vLLM/SGLang/Unsloth support. API available.
- **Claude Fable 5.2 / Mythos 5.2** — Closed frontier. API on Anthropic, AWS, Google Cloud, Microsoft Foundry. $8/$40. Mythos gated. Brushstroke image gen capability.
- **Gemini 4 Hydrogen / Carbon / Neon** — Closed. Hydrogen $1.50/$7.50 widely available incl. free AI Studio; Neon $3/$15; Carbon intro pricing ends Nov 30.
- **Muse Ember** — Closed small agent model. API $0.10/$0.50.
- **Kimi K3.1 Pro** — Open weights on HF (2.8T MoE, ~1.56TB). Serve with vLLM, SGLang, or TokenSpeed. Multi-node recommended; quantized options emerging. API also available. Dominating HF.
- **Ripple-65B Preview** — Dense 65B on HF (Apache 2.0). Available on Together AI, GMI Cloud, OpenRouter. Quantized builds fit MacBook / DGX Spark.
- **GPT-6 Cyber** — Closed specialized model for authorized cyber research. Restricted to Daybreak Red customers via API/Codex. Not self-hostable.
- **Gemini Omni 1.2 Flash** — API for longer (15s), cheaper video gen/editing.
- **DeepSeek dsh-superagent + Harness** — Local MIT coding agent that watches a GitHub repo and executes requests in isolated workers. Runs on user machine.
- **Nace Drex Max v1** — Open 27B decision model for local agent decisions (probabilities over options). GGUF/llama.cpp/Ollama support; Apple Silicon and NVIDIA friendly.
- **Baseten joey-1** — Tiny 2B decision model (MIT on HF) for calibrated labels at very low API cost.
- **Mistral Large 4** — Open weights on HF; API available. Fine-tuning via TRL 1.17+ (LoRA on single high-end node). Full inference requires significant multi-node resources; quantized/serving recipes emerging.
- **Hydrogen-1.0** — Open MIT weights (gated on HF); scientific MoE runnable on multi-GPU (tested on 8 GPUs with SGLang). Quantized variants for Blackwell/AMD.
- **Pika H3 Flex** — Open weights + Diffusers/ComfyUI support for local video+audio gen. High VRAM needs (H100-class for full). API for lower-cost hosted use.
- **LFM3 local stacks** — GGUF/MLX/ONNX/FP8 for LiquidAI LFM3 family; single-GPU fine-tune + edge inference (llama.cpp, MLX, vLLM, Transformers). High recent HF activity.
- **DeepInfer** — DeepSeek production stack; high efficiency; dual hardware. NVFP4 variants for reduced download/size on Blackwell.
- **FreeToken** — Apache-2.0 edge-native MoE serving engine. Pools GPU + CPU + system RAM for large models (DeepSeek Flash, Qwen, GLM) on gaming PCs/laptops. OpenAI/Anthropic-compatible APIs. Strong for models that don't fully fit in VRAM. Desktop app + CLI available.
- **vLLM / SGLang / llama.cpp / TensorRT-LLM** — primary for large open MoEs and dense models. llama.cpp v1.0.0 adds API stability, FP8 KV, MoE expert cache. Day-0 support for new releases including Inkling 2 Mini/Small, ERNIE.
- **Ollama / Unsloth / llama.cpp / MLX** — excellent for local small models and Dynamic V3.1 GGUFs (Qwen3.8-27B high accuracy on 12GB+). Inkling Mini and Ternary Bonsai practical.
- **Hugging Face Spaces + Hub + Inference** — models, ZeroGPU, demos.
- **Diffusers + ComfyUI** — image/video pipelines (MiniMax-H3-Image native 4K, PAN 2, LTX-2.5, Kandinsky, Pika, SenseNova U1.6, etc.)
- Voice agent SDKs; specialized scientific models.
- Coding agents with free tiers: GitHub Copilot Free, Cline (open), Kilo Code, opencode, Claude Code, Cursor, Google Antigravity, OpenHands, etc. Rankings (Nov 2026): Claude Code top by usage/merge rates, followed by Codex, Copilot, Cursor.
- Cloudflare Pages + Workers for free full-stack AI app hosting.
- Ranked hosting platforms: Baseten (managed APIs, free plan, top ranked), BentoML, NVIDIA Triton Inference Server (open-source).
- Tools like gpu-free-serve: Tunnel Colab/Kaggle free GPUs as local OpenAI-compatible endpoints via cloudflared/ngrok for editor integration.

## Agent & Developer Tooling

- **Shirudo** — agent-driven eBPF shields for runtime Linux protection without restarts
- **Claude Ship** — automated GitHub PR review/patch/approval agents
- **dsh-superagent** — local router-worker coding agent for GitHub repos
- **Drex Max / joey-1** — open decision models for efficient agent loops (computer-use, routing)
- **LFM3** — open multimodal family for specialized local agents and fine-tuning
- **Agensh** — open decentralized multi-agent harness for scaling coding agent organizations (up to 1,024)
- Local coding agents (Flint on laptop)
- Local conversational agents / NPCs (Nemotron Bolt E4B)
- Agent harnesses for Flash models and new teachers; self-hosted options for Mistral Large 4, Kimi K3.1 Pro, Inkling 2 Mini/Small, LongCat-2.5, Ling family, ERNIE, Bonsai
- MCP, tool-calling, memory systems
- On-device stacks (LFM3, Flint, Muse Glimmer, Bolt E4B, FreeToken for larger MoEs, Unsloth GGUFs, Inkling Mini, Ternary Bonsai)
- TRL for post-training (v1.19 multi-teacher distillation, faster SFT); accelerator backends
- Microsoft TokenEconomizer: free tool cutting AI coding token costs by up to 31%
- DeepMind agent demos and scientific automation
- GitHub Copilot in Xcode; Google Antigravity agent-first IDE; Cline as top open agentic coding tool; OpenHands
- Anthropic Claude Whiteboards, Sheets (beta), Data (GA) for collaborative AI workspaces
- Tencent LoopForge: self-hosted sandboxed coding agent workspace (MIT)
- Cognition SWE-2.1 coding model

## Developer Focus Areas (current)

- Testing GLM-5.4 Loop Transformer for generalized coding (vision + code for creative/3D tasks) once API/weights available
- Evaluating Qwen4-Max efficiency claims vs Gemini 4 Neon / Claude Fable 5.2 on long-horizon agentic and coding tasks
- Experimenting with newly open LongCat-2.5 (MIT, large VRAM) for self-hosted multimodal agents
- Running high-accuracy local Qwen3.8-27B, Inkling 2 Mini, and Ternary Bonsai via Unsloth/GGUF on consumer hardware
- Experimenting with Inkling 2 Mini/Small, ERNIE 5.5 Flash, Ling-3.2-air, and continuing Kimi K3.1 Pro / Ripple-65B for self-hosted agentic coding
- Authorized use of GPT-6 Cyber for defensive vulnerability research (restricted access); Mythos 5.2 for vetted programs
- Experimenting with local coding agents (dsh-superagent, Cline, LoopForge, Claude Ship) and decision layers (Drex Max, joey-1) for efficient agent workflows
- Running large MoEs locally via FreeToken on consumer hardware (GPU+CPU+RAM pooling)
- Testing open video/image generation stacks (MiniMax H3-Image native 4K via ComfyUI/Diffusers, Pika H3 Flex, LTX-2.5, SenseNova U1.6, Fable brushstroke method, Gemini Omni API) and trending HF models (Inkling, idol, uncensored variants, Qwen, Arete)
- Leveraging free tiers, NIM, Run:ai self-host, non-NVIDIA options; cost optimization with TokenEconomizer; Shadeform for cheap H100 access; Together AI preemptible for 50% savings on interruptible jobs
- Scientific and public-sector agent tools; medical models (LingSante)
- Robotics world-action models and formal verification agents
- Evaluating Shirudo for agent-native runtime security on Linux
- Testing Claude Code / Codex / Cursor rankings for real merge rates and agent workflows
- Using TRL multi-teacher distillation for efficient post-training

---

*When a free tier changes or a tool is superseded, edit the existing row/bullet instead of appending a near-duplicate.*
