# Tools & Compute

Living reference for free/low-cost GPUs, hosting, inference stacks, and developer tooling. Quotas and offerings change; update entries in place.

**Last refined:** 2026-11-02

---

## Free / Low-Cost GPU Access

| Provider | What you get | Notes / Limits |
|----------|--------------|----------------|
| Google Colab (free) | Hosted notebook, limited T4 | Session limits (~12h); quota fluctuates |
| Kaggle Notebooks | T4 ×2, ~30h/week | Phone verification; multi-GPU / TPU options |
| Hugging Face ZeroGPU | Shared RTX Pro 6000 Blackwell for Gradio Spaces | Short daily quota (minutes); demo-oriented |
| NVIDIA NIM / build.nvidia.com | Free endpoints for many open models (Nemotron, DeepSeek-V4.1-Flash, GLM, Muse, Gemma, etc.) | OpenAI-compatible; NVIDIA Developer Program key (phone verification in supported countries). Rate limits vary. |
| Groq free tier | Fast inference on supported models (gpt-oss, Qwen3.8-27B, etc.) | Rate limits (e.g. 30 RPM / 1k RPD for coding models); no card |
| Google AI Studio / Gemini free | Flash models (Gemini 3.x family), Gemma 4 | May train on prompts; usage per model; no card for free tier |
| OpenRouter free | Limited free models / daily requests (Nemotron, Gemma, Inkling, etc.) | Card-free options; ~50-1000 requests/day depending on plan |
| Cloudflare Workers AI | 10k neurons/day | Edge inference |
| Requesty / AIHubMix / other aggregators | Free model routes | Card-free free plans with daily quotas |
| Modal / Lightning AI | Free monthly compute / studios | Check current balances (e.g. Modal $30/mo) |
| NVIDIA Run:ai (open-sourced) | Full GPU orchestration (Apache 2.0) | Self-host; supply own K8s/GPUs |
| Startup programs | Credit grants | Vary (e.g. Inference.net up to $10k) |
| RunPod / Vast.ai | Cheap spot GPUs | Paid but low $/hr |

## Hosting & Serving

- **DeepSeek dsh-superagent + Harness** — Local MIT coding agent that watches a GitHub repo and executes requests in isolated workers. Runs on user machine.
- **Nace Drex Max v1** — Open 27B decision model for local agent decisions (probabilities over options). GGUF/llama.cpp/Ollama support; Apple Silicon and NVIDIA friendly.
- **Baseten joey-1** — Tiny 2B decision model (MIT on HF) for calibrated labels at very low API cost.
- **Mistral Large 4** — Open weights on HF; API available. Fine-tuning via TRL (LoRA on high-end nodes). Full inference requires significant multi-node resources; quantized/serving recipes emerging.
- **Pika H3 Flex** — Open weights + Diffusers/ComfyUI support for local video+audio gen. High VRAM needs (H100-class for full). API for lower-cost hosted use.
- **LFM3 local stacks** — GGUF/MLX/ONNX/FP8 for LiquidAI LFM3 family; single-GPU fine-tune + edge inference (llama.cpp, MLX, vLLM, Transformers). High recent HF activity.
- **DeepInfer** — DeepSeek production stack; high efficiency; dual hardware. NVFP4 variants for reduced download/size on Blackwell.
- **FreeToken** — Apache-2.0 edge-native MoE serving engine. Pools GPU + CPU + system RAM for large models (DeepSeek Flash, Qwen, GLM) on gaming PCs/laptops. OpenAI/Anthropic-compatible APIs. Strong for models that don't fully fit in VRAM. Desktop app + CLI available.
- **vLLM / SGLang / llama.cpp / TensorRT-LLM** — primary for large open MoEs and dense models (Nanbeige TP=4, Beam, Muse, DeepSeek, MiniMax, Nemotron, upcoming Kimi, Mistral Large 4)
- **Ollama / Unsloth / llama.cpp / MLX** — excellent for local small models like LFM3, Nemotron Bolt E4B, Flint, Drex Max quantizations, and emerging Nanbeige quantizations (e.g. NVFP4). CPU GGUF options like POCKET-Darwin-180B.
- **Hugging Face Spaces + Hub + Inference** — models, ZeroGPU, Carbon-X demos, TorchNeuron
- **Diffusers + ComfyUI** — image/video pipelines (FLUX.3 Image Klein with layout control, Pika H3 Flex, LTX-2.5, Kandinsky 6 etc.)
- Voice agent SDKs (Voxtral 3 + LiveKit); Dessa research preview waitlist
- Specialized: Carbon-X for DNA/genomics workflows; Liquid API/Playground for LFM3
- Replit for Government: access to intelligence and custom tool-building for public servants.
- Coding agents with free tiers: GitHub Copilot Free, opencode, Kilo Code, etc.

## Agent & Developer Tooling

- **dsh-superagent** — local router-worker coding agent for GitHub repos
- **Drex Max / joey-1** — open decision models for efficient agent loops (computer-use, routing)
- **LFM3** — open multimodal family for specialized local agents and fine-tuning
- **Agensh** — open decentralized multi-agent harness for scaling coding agent organizations (up to 1,024)
- Local coding agents (Flint on laptop)
- Local conversational agents / NPCs (Nemotron Bolt E4B)
- Agent harnesses for Flash models (MiniMax, DeepSeek) and new teachers (Nanbeige); self-hosted options for Mistral Large 4 cyber/coding use cases
- MCP, tool-calling, memory systems
- On-device stacks (LFM3, Flint, Muse Glimmer, Bolt E4B, FreeToken for larger MoEs)
- TRL for post-training (incl. Mistral Large 4 examples); accelerator backends (TorchNeuron, TorchTPU)
- Microsoft TokenEconomizer: free tool cutting AI coding token costs by up to 31%
- DeepMind agent demos (prompt-to-physical robot) and scientific automation (gene therapy injection, forest mapping)

## Developer Focus Areas (current)

- Experimenting with local coding agents (dsh-superagent) and decision layers (Drex Max, joey-1) for efficient agent workflows
- Running large MoEs locally via FreeToken on consumer hardware (GPU+CPU+RAM pooling)
- Experimenting with large open-weight models for self-hosted control (Mistral Large 4 for coding/cyber)
- Testing open video generation stacks (Pika H3 Flex via Diffusers/ComfyUI) and trending HF models (DeepSeek Flash, LFM3, Qwen)
- Experimenting with LFM3 family for multimodal local agents and single-GPU specialization
- Experimenting with multi-agent scaling via open Agensh
- Running new local models (LFM3, Flint, Nemotron Bolt E4B, Drex Max) and specialized scientific models (Carbon-X, Rosalind biology)
- Evaluating MiniMax M3.1 Flash open weights and preparing for Kimi K3.1 Pro open weights (Nov 4); testing Nanbeige4.3-33B on multi-GPU or quant
- Serving efficient MoEs with open stacks; speech research (Dessa, Nemotron Transcribe)
- Leveraging free tiers, NIM, Run:ai self-host, non-NVIDIA options; cost optimization with TokenEconomizer
- Scientific and public-sector agent tools (PlanAssist, Replit for Government, ForTy forest map)

---

*When a free tier changes or a tool is superseded, edit the existing row/bullet instead of appending a near-duplicate.*
