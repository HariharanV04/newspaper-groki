# Tools & Compute

Living reference for free/low-cost GPUs, hosting, inference stacks, and developer tooling. Quotas and offerings change; update entries in place.

**Last refined:** 2026-10-23

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

- **DeepInfer** — DeepSeek production stack; high efficiency; dual hardware
- **vLLM / SGLang / llama.cpp / TensorRT-LLM** — primary for large open MoEs (Beam, Muse, DeepSeek, MiniMax, Nemotron); day-0 support common
- **Hugging Face Spaces + Hub + Inference** — models, ZeroGPU, Carbon-X demos, TorchNeuron
- **Diffusers + ComfyUI** — image/video pipelines
- Voice agent SDKs (Voxtral 3 + LiveKit)
- Specialized: Carbon-X for DNA/genomics workflows

## Agent & Developer Tooling

- Local coding agents (Flint on laptop)
- Agent harnesses for Flash models (MiniMax, DeepSeek)
- MCP, tool-calling, memory systems
- On-device stacks (Flint, Muse Glimmer)
- TRL for post-training; accelerator backends (TorchNeuron, TorchTPU)

## Developer Focus Areas (current)

- Running new local models (Flint) and specialized scientific models (Carbon-X)
- Evaluating MiniMax M3.1 Flash open weights
- Serving efficient MoEs with open stacks
- Voice agents and proactive agents (Claude Duet style)
- Leveraging free tiers, NIM, Run:ai self-host, non-NVIDIA options

---

*When a free tier changes or a tool is superseded, edit the existing row/bullet instead of appending a near-duplicate.*
