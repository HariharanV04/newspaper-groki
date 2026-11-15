# Tools & Compute

Living reference for free/low-cost GPUs, hosting, inference stacks, and developer tooling. Quotas and offerings change; update entries in place.

**Last refined:** 2026-11-15

---

## Free / Low-Cost GPU Access

| Provider | What you get | Notes / Limits |
|----------|--------------|----------------|
| Google Colab (free) | Hosted notebook, limited T4 | Session limits (~12h); quota fluctuates |
| Kaggle Notebooks | T4 ×2, ~30h/week | Phone verification; multi-GPU / TPU options |
| Hugging Face ZeroGPU | Shared RTX Pro 6000 Blackwell for Gradio Spaces | Short daily quota (minutes); demo-oriented |
| NVIDIA NIM / build.nvidia.com | Free endpoints for many open models (Nemotron, DeepSeek-V4.1-Flash, GLM, Muse, Gemma, etc.) | OpenAI-compatible; NVIDIA Developer Program key (phone verification in supported countries). Rate limits vary. |
| Groq free tier | Fast inference on supported models (gpt-oss, Qwen3.8-27B, etc.) | Rate limits (e.g. 30 RPM / 1k RPD for coding models); no card |
| Google AI Studio / Gemini free | Flash/Hydrogen models (Gemini family + Omni), Gemma 4 | May train on prompts; usage per model; no card for free tier. Hydrogen available. |
| OpenRouter free | Limited free models / daily requests (Nemotron, Gemma, Inkling, Ling-3.2-flash 1M free, etc.) | Card-free options; ~50-1000 requests/day depending on plan |
| Cloudflare Workers AI | 10k neurons/day | Edge inference |
| SambaNova Cloud | Free use of hosted open models until payment method linked | Rate limits apply |
| Requesty / AIHubMix / other aggregators | Free model routes | Card-free free plans with daily quotas |
| Modal | $30 free compute credits/month | Starter plan, no monthly fee, GPU concurrency; startup programs available |
| Lightning AI | Free monthly compute / studios | Check current balances (e.g. up to ~30 credits / ~50 GPU hours on T4 + free Studio) |
| Daytona | $200 free compute for new accounts | Sandboxes for AI agents; no card |
| AMD Developer Cloud | $100 complimentary credit on Instinct MI300X | Approved developers via AI Developer Program |
| IteraCompute / others | Free token routes (e.g. up to 30M tokens/month Auto on open models) | No card for some; rate limited |
| NVIDIA Run:ai (open-sourced) | Full GPU orchestration (Apache 2.0) | Self-host; supply own K8s/GPUs |
| Startup programs | Credit grants | Vary (e.g. Inference.net up to $10k, Hostkey GPU grants, Novita, Google/AWS/Microsoft, GMI Cloud, fal, Together AI, Baseten, etc.) |
| RunPod / Vast.ai | Cheap spot GPUs | Paid but low $/hr |

## Hosting & Serving

- **MiniMax H3-Image** — Open weights on HF for native 4K T2I + multi-ref editing. ComfyUI native; quantized options emerging. Community license (regional exclusions). API also available.
- **Unsloth Dynamic V3.1 GGUFs** — Highest-accuracy local builds for Qwen3.8-27B (and related) on 12GB+ RAM via llama.cpp / Unsloth Desktop.
- **Inkling 2 Small** — Open Apache 2.0 weights on HF (594B/17B MoE). Day-0 vLLM/SGLang/Unsloth support. API available.
- **Claude Fable 5.2 / Mythos 5.2** — Closed frontier. API on Anthropic, AWS, Google Cloud, Microsoft Foundry. $8/$40. Mythos gated.
- **Gemini 4 Hydrogen / Carbon** — Closed. Hydrogen $1.50/$7.50 widely available incl. free AI Studio; Carbon intro pricing ends Nov 30.
- **Muse Ember** — Closed small agent model. API $0.10/$0.50.
- **LongCat-2.5** — Full MIT weights on HF (1.6T MoE). Serve with vLLM/SGLang once recipes mature; API available.
- **Kimi K3.1 Pro** — Open weights on HF (2.8T MoE, ~1.56TB). Serve with vLLM, SGLang, or TokenSpeed. Multi-node recommended; quantized options emerging. API also available. Dominating HF.
- **Ripple-65B Preview** — Dense 65B on HF (Apache 2.0). Available on Together AI, GMI Cloud, OpenRouter. Quantized builds fit MacBook / DGX Spark.
- **GPT-6 Cyber** — Closed specialized model for authorized cyber research. Restricted to Daybreak Red customers via API/Codex. Not self-hostable.
- **Gemini Omni 1.2 Flash** — API for longer (15s), cheaper video gen/editing.
- **DeepSeek dsh-superagent + Harness** — Local MIT coding agent that watches a GitHub repo and executes requests in isolated workers. Runs on user machine.
- **Nace Drex Max v1** — Open 27B decision model for local agent decisions (probabilities over options). GGUF/llama.cpp/Ollama support; Apple Silicon and NVIDIA friendly.
- **Baseten joey-1** — Tiny 2B decision model (MIT on HF) for calibrated labels at very low API cost.
- **Mistral Large 4** — Open weights on HF; API available. Fine-tuning via TRL 1.17 (LoRA on single high-end node). Full inference requires significant multi-node resources; quantized/serving recipes emerging.
- **Hydrogen-1.0** — Open MIT weights (gated on HF); scientific MoE runnable on multi-GPU (tested on 8 GPUs with SGLang). Quantized variants for Blackwell/AMD.
- **Pika H3 Flex** — Open weights + Diffusers/ComfyUI support for local video+audio gen. High VRAM needs (H100-class for full). API for lower-cost hosted use.
- **LFM3 local stacks** — GGUF/MLX/ONNX/FP8 for LiquidAI LFM3 family; single-GPU fine-tune + edge inference (llama.cpp, MLX, vLLM, Transformers). High recent HF activity.
- **DeepInfer** — DeepSeek production stack; high efficiency; dual hardware. NVFP4 variants for reduced download/size on Blackwell.
- **FreeToken** — Apache-2.0 edge-native MoE serving engine. Pools GPU + CPU + system RAM for large models (DeepSeek Flash, Qwen, GLM) on gaming PCs/laptops. OpenAI/Anthropic-compatible APIs. Strong for models that don't fully fit in VRAM. Desktop app + CLI available.
- **vLLM / SGLang / llama.cpp / TensorRT-LLM** — primary for large open MoEs and dense models. llama.cpp v1.0.0 adds API stability, FP8 KV, MoE expert cache. Day-0 support for new releases including Inkling 2 Small.
- **Ollama / Unsloth / llama.cpp / MLX** — excellent for local small models and Dynamic V3.1 GGUFs (Qwen3.8-27B high accuracy on 12GB+).
- **Hugging Face Spaces + Hub + Inference** — models, ZeroGPU, demos.
- **Diffusers + ComfyUI** — image/video pipelines (MiniMax-H3-Image native 4K, PAN 2, LTX-2.5, Kandinsky, Pika, etc.)
- Voice agent SDKs; specialized scientific models.
- Coding agents with free tiers: GitHub Copilot Free, Cline (open), Kilo Code, opencode, Claude Code, Cursor, Google Antigravity, etc.
- Cloudflare Pages + Workers for free full-stack AI app hosting.
- Ranked hosting platforms: Baseten (managed APIs, free plan, top ranked), BentoML, NVIDIA Triton Inference Server (open-source).

## Agent & Developer Tooling

- **dsh-superagent** — local router-worker coding agent for GitHub repos
- **Drex Max / joey-1** — open decision models for efficient agent loops (computer-use, routing)
- **LFM3** — open multimodal family for specialized local agents and fine-tuning
- **Agensh** — open decentralized multi-agent harness for scaling coding agent organizations (up to 1,024)
- Local coding agents (Flint on laptop)
- Local conversational agents / NPCs (Nemotron Bolt E4B)
- Agent harnesses for Flash models and new teachers; self-hosted options for Mistral Large 4, Kimi K3.1 Pro, Inkling 2 Small
- MCP, tool-calling, memory systems
- On-device stacks (LFM3, Flint, Muse Glimmer, Bolt E4B, FreeToken for larger MoEs, Unsloth GGUFs)
- TRL for post-training; accelerator backends
- Microsoft TokenEconomizer: free tool cutting AI coding token costs by up to 31%
- DeepMind agent demos and scientific automation
- GitHub Copilot in Xcode; Google Antigravity agent-first IDE; Cline as top open agentic coding tool
- Anthropic Claude Whiteboards, Sheets (beta), Data (GA) for collaborative AI workspaces

## Developer Focus Areas (current)

- Evaluating Claude Fable 5.2 vs Gemini 4 Hydrogen/Carbon on coding/science tasks (price/performance tradeoffs; Carbon intro pricing ends Nov 30)
- Running high-accuracy local Qwen3.8-27B via Unsloth Dynamic V3.1 GGUFs on consumer hardware
- Experimenting with newly open Inkling 2 Small and continuing Kimi K3.1 Pro / Ripple-65B / LongCat-2.5 for self-hosted agentic coding and long-horizon tasks
- Authorized use of GPT-6 Cyber for defensive vulnerability research (restricted access); Mythos 5.2 for vetted programs
- Experimenting with local coding agents (dsh-superagent, Cline) and decision layers (Drex Max, joey-1) for efficient agent workflows
- Running large MoEs locally via FreeToken on consumer hardware (GPU+CPU+RAM pooling)
- Testing open video/image generation stacks (MiniMax H3-Image native 4K via ComfyUI/Diffusers, Pika H3 Flex, LTX-2.5, Gemini Omni API) and trending HF models (idol, uncensored variants, Qwen, Arete)
- Leveraging free tiers, NIM, Run:ai self-host, non-NVIDIA options; cost optimization with TokenEconomizer
- Scientific and public-sector agent tools
- Robotics world-action models and formal verification agents

---

*When a free tier changes or a tool is superseded, edit the existing row/bullet instead of appending a near-duplicate.*
