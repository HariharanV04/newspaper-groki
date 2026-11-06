# Tools & Compute

Living reference for free/low-cost GPUs, hosting, inference stacks, and developer tooling. Quotas and offerings change; update entries in place.

**Last refined:** 2026-11-06

---

## Free / Low-Cost GPU Access

| Provider | What you get | Notes / Limits |
|----------|--------------|----------------|
| Google Colab (free) | Hosted notebook, limited T4 | Session limits (~12h); quota fluctuates |
| Kaggle Notebooks | T4 ×2, ~30h/week | Phone verification; multi-GPU / TPU options |
| Hugging Face ZeroGPU | Shared RTX Pro 6000 Blackwell for Gradio Spaces | Short daily quota (minutes); demo-oriented |
| NVIDIA NIM / build.nvidia.com | Free endpoints for many open models (Nemotron, DeepSeek-V4.1-Flash, GLM, Muse, Gemma, etc.) | OpenAI-compatible; NVIDIA Developer Program key (phone verification in supported countries). Rate limits vary. |
| Groq free tier | Fast inference on supported models (gpt-oss, Qwen3.8-27B, etc.) | Rate limits (e.g. 30 RPM / 1k RPD for coding models); no card |
| Google AI Studio / Gemini free | Flash models (Gemini 3.x family + Omni), Gemma 4 | May train on prompts; usage per model; no card for free tier. Omni 1.2 Flash available. |
| OpenRouter free | Limited free models / daily requests (Nemotron, Gemma, Inkling, etc.) | Card-free options; ~50-1000 requests/day depending on plan |
| Cloudflare Workers AI | 10k neurons/day | Edge inference |
| SambaNova Cloud | Free use of hosted open models until payment method linked | Rate limits apply |
| Requesty / AIHubMix / other aggregators | Free model routes | Card-free free plans with daily quotas |
| Modal / Lightning AI | Free monthly compute / studios | Check current balances (e.g. Modal $30/mo + startup credits up to $25k) |
| NVIDIA Run:ai (open-sourced) | Full GPU orchestration (Apache 2.0) | Self-host; supply own K8s/GPUs |
| Startup programs | Credit grants | Vary (e.g. Inference.net up to $10k, Hostkey GPU grants, Novita, Google/AWS/Microsoft) |
| RunPod / Vast.ai | Cheap spot GPUs | Paid but low $/hr |

## Hosting & Serving

- **Kimi K3.1 Pro** — Open weights on HF (2.8T MoE, ~1.56TB). Serve with vLLM, SGLang, or TokenSpeed. Multi-node recommended; quantized options emerging. API also available. Dominating HF.
- **Ripple-65B Preview** — Dense 65B on HF (Apache 2.0). Available on Together AI, GMI Cloud, OpenRouter. Quantized builds fit MacBook / DGX Spark.
- **GPT-6 Cyber** — Closed specialized model for authorized cyber research. Restricted to Daybreak Red customers via API/Codex. Not self-hostable.
- **Gemini Omni 1.2 Flash** — API for longer (15s), cheaper video gen/editing.
- **DeepSeek dsh-superagent + Harness** — Local MIT coding agent that watches a GitHub repo and executes requests in isolated workers. Runs on user machine.
- **Nace Drex Max v1** — Open 27B decision model for local agent decisions (probabilities over options). GGUF/llama.cpp/Ollama support; Apple Silicon and NVIDIA friendly.
- **Baseten joey-1** — Tiny 2B decision model (MIT on HF) for calibrated labels at very low API cost.
- **Mistral Large 4** — Open weights on HF; API available. Fine-tuning via TRL 1.17 (LoRA on single high-end node). Full inference requires significant multi-node resources; quantized/serving recipes emerging.
- **Hydrogen-1.0** — Open MIT weights (gated on HF); scientific MoE runnable on multi-GPU (tested on 8 GPUs with SGLang). Quantized variants for Blackwell/AMD.
- **LongCat-2.5** — API available now (low limited-time pricing); weights coming soon for self-hosting.
- **Pika H3 Flex** — Open weights + Diffusers/ComfyUI support for local video+audio gen. High VRAM needs (H100-class for full). API for lower-cost hosted use.
- **LFM3 local stacks** — GGUF/MLX/ONNX/FP8 for LiquidAI LFM3 family; single-GPU fine-tune + edge inference (llama.cpp, MLX, vLLM, Transformers). High recent HF activity.
- **DeepInfer** — DeepSeek production stack; high efficiency; dual hardware. NVFP4 variants for reduced download/size on Blackwell.
- **FreeToken** — Apache-2.0 edge-native MoE serving engine. Pools GPU + CPU + system RAM for large models (DeepSeek Flash, Qwen, GLM) on gaming PCs/laptops. OpenAI/Anthropic-compatible APIs. Strong for models that don't fully fit in VRAM. Desktop app + CLI available.
- **vLLM / SGLang / llama.cpp / TensorRT-LLM** — primary for large open MoEs and dense models (Nanbeige TP=4, Beam, Muse, DeepSeek, MiniMax, Nemotron, Kimi K3.1 Pro, Mistral Large 4, Ripple-65B). llama.cpp v0.9.0 adds native FP8 and multi-node TP. Day-0 support for new releases.
- **Ollama / Unsloth / llama.cpp / MLX** — excellent for local small models like LFM3, Nemotron Bolt E4B, Flint, Drex Max quantizations, and emerging Nanbeige quantizations (e.g. NVFP4). CPU GGUF options like POCKET-Darwin-180B.
- **Hugging Face Spaces + Hub + Inference** — models, ZeroGPU, Carbon-X demos, TorchNeuron
- **Diffusers + ComfyUI** — image/video pipelines (FLUX.3 Image Klein with layout control, Pika H3 Flex, LTX-2.5, Kandinsky 6, P-H3-Image, Gemini Omni via API etc.)
- Voice agent SDKs (Voxtral 3 + LiveKit); Dessa research preview waitlist
- Specialized: Carbon-X for DNA/genomics workflows; Liquid API/Playground for LFM3
- Replit for Government: access to intelligence and custom tool-building for public servants.
- Coding agents with free tiers: GitHub Copilot Free (now also in Xcode), Cline (highly recommended open), Kilo Code, opencode, Claude Code, Cursor, Google Antigravity, etc.
- Cloudflare Pages + Workers for free full-stack AI app hosting (unlimited bandwidth options).
- Together AI continuous inference optimization compiler (reported up to 2.6x speedups).

## Agent & Developer Tooling

- **dsh-superagent** — local router-worker coding agent for GitHub repos
- **Drex Max / joey-1** — open decision models for efficient agent loops (computer-use, routing)
- **LFM3** — open multimodal family for specialized local agents and fine-tuning
- **Agensh** — open decentralized multi-agent harness for scaling coding agent organizations (up to 1,024)
- Local coding agents (Flint on laptop)
- Local conversational agents / NPCs (Nemotron Bolt E4B)
- Agent harnesses for Flash models (MiniMax, DeepSeek) and new teachers (Nanbeige); self-hosted options for Mistral Large 4 and Kimi K3.1 Pro cyber/coding use cases
- MCP, tool-calling, memory systems
- On-device stacks (LFM3, Flint, Muse Glimmer, Bolt E4B, FreeToken for larger MoEs)
- TRL for post-training (incl. Mistral Large 4 single-node LoRA, multi-teacher distillation); accelerator backends (TorchNeuron, TorchTPU)
- Microsoft TokenEconomizer: free tool cutting AI coding token costs by up to 31%
- DeepMind agent demos (prompt-to-physical robot) and scientific automation (gene therapy injection, forest mapping)
- GitHub Copilot in Xcode; Google Antigravity agent-first IDE; Cline as top open agentic coding tool

## Developer Focus Areas (current)

- Experimenting with newly open Kimi K3.1 Pro and Ripple-65B for self-hosted agentic coding and long-horizon tasks
- Authorized use of GPT-6 Cyber for defensive vulnerability research (restricted access)
- Experimenting with local coding agents (dsh-superagent, Cline) and decision layers (Drex Max, joey-1) for efficient agent workflows
- Running large MoEs locally via FreeToken on consumer hardware (GPU+CPU+RAM pooling)
- Experimenting with large open-weight models for self-hosted control (Mistral Large 4 for coding/cyber, Hydrogen-1.0 for science, Kimi K3.1 Pro)
- Testing open video generation stacks (Pika H3 Flex, LTX-2.5 via Diffusers/ComfyUI, Gemini Omni API) and trending HF models (Kimi, DeepSeek Flash, LFM3, Qwen)
- Experimenting with LFM3 family for multimodal local agents and single-GPU specialization
- Experimenting with multi-agent scaling via open Agensh
- Running new local models (LFM3, Flint, Nemotron Bolt E4B, Drex Max) and specialized scientific models (Carbon-X, Rosalind biology, Hydrogen-1.0)
- Evaluating MiniMax M3.1 Flash open weights and Kimi K3.1 Pro; testing Nanbeige4.3-33B on multi-GPU or quant
- Serving efficient MoEs with open stacks; speech research (Dessa, Nemotron Transcribe); image/video gen with Omni and Images 2.6
- Leveraging free tiers, NIM, Run:ai self-host, non-NVIDIA options; cost optimization with TokenEconomizer and Together compiler
- Scientific and public-sector agent tools (PlanAssist, Replit for Government, ForTy forest map)

---

*When a free tier changes or a tool is superseded, edit the existing row/bullet instead of appending a near-duplicate.*
