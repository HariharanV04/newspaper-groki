# Tools & Compute

Living reference for free/low-cost GPUs, hosting, inference stacks, and developer tooling. Quotas and offerings change; update entries in place.

**Last refined:** 2026-10-28

---

## Free / Low-Cost GPU Access

| Provider | What you get | Notes / Limits |
|----------|--------------|----------------|
| Google Colab (free) | Hosted notebook, limited T4 | Session limits (~12h); quota fluctuates |
| Kaggle Notebooks | T4 ×2, ~30h/week | Phone verification; multi-GPU / TPU options |
| Hugging Face ZeroGPU | Shared RTX Pro 6000 Blackwell for Gradio Spaces | Short daily quota (minutes); demo-oriented |
| NVIDIA NIM / build.nvidia.com | Free endpoints for many open models | OpenAI-compatible; no card for free tier |
| Groq free tier | Fast inference on supported models | Rate limits; no card |
| Google AI Studio / Gemini free | Flash models, limited daily | May train on data; no card |
| OpenRouter free | Limited free models / daily requests | Card-free options |
| Cloudflare Workers AI | 10k neurons/day | Edge inference |
| Modal / Lightning AI | Free monthly compute / studios | Check current balances |
| NVIDIA Run:ai (open-sourced) | Full GPU orchestration (Apache 2.0) | Self-host; supply own K8s/GPUs |
| Startup programs | Credit grants | Vary |
| RunPod / Vast.ai | Cheap spot GPUs | Paid but low $/hr |

## Hosting & Serving

- **LFM3 local stacks** — GGUF/MLX/ONNX/FP8 for LiquidAI LFM3 family; single-GPU fine-tune + edge inference (llama.cpp, MLX, vLLM, Transformers)
- **DeepInfer** — DeepSeek production stack; high efficiency; dual hardware
- **vLLM / SGLang / llama.cpp / TensorRT-LLM** — primary for large open MoEs and dense models (Nanbeige TP=4, Beam, Muse, DeepSeek, MiniMax, Nemotron, upcoming Kimi)
- **Ollama / Unsloth / llama.cpp / MLX** — excellent for local small models like LFM3, Nemotron Bolt E4B, Flint, and emerging Nanbeige quantizations (e.g. NVFP4)
- **Hugging Face Spaces + Hub + Inference** — models, ZeroGPU, Carbon-X demos, TorchNeuron
- **Diffusers + ComfyUI** — image/video pipelines (FLUX.3 Image Klein with layout control, Kandinsky 6 etc.)
- Voice agent SDKs (Voxtral 3 + LiveKit); Dessa research preview waitlist
- Specialized: Carbon-X for DNA/genomics workflows; Liquid API/Playground for LFM3

## Agent & Developer Tooling

- **LFM3** — open multimodal family for specialized local agents and fine-tuning
- **Agensh** — open decentralized multi-agent harness for scaling coding agent organizations (up to 1,024)
- Local coding agents (Flint on laptop)
- Local conversational agents / NPCs (Nemotron Bolt E4B)
- Agent harnesses for Flash models (MiniMax, DeepSeek) and new teachers (Nanbeige)
- MCP, tool-calling, memory systems
- On-device stacks (LFM3, Flint, Muse Glimmer, Bolt E4B)
- TRL for post-training; accelerator backends (TorchNeuron, TorchTPU)

## Developer Focus Areas (current)

- Experimenting with LFM3 family for multimodal local agents and single-GPU specialization
- Experimenting with multi-agent scaling via open Agensh
- Running new local models (LFM3, Flint, Nemotron Bolt E4B) and specialized scientific models (Carbon-X)
- Evaluating MiniMax M3.1 Flash open weights and preparing for Kimi K3.1 Pro open weights; testing Nanbeige4.3-33B on multi-GPU or quant
- Serving efficient MoEs with open stacks; speech research (Dessa)
- Leveraging free tiers, NIM, Run:ai self-host, non-NVIDIA options

---

*When a free tier changes or a tool is superseded, edit the existing row/bullet instead of appending a near-duplicate.*
