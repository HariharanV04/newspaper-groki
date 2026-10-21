# Tools & Compute

Living reference for free/low-cost GPUs, hosting, inference stacks, and developer tooling. Quotas and offerings change; update entries in place.

**Last refined:** 2026-10-21

---

## Free / Low-Cost GPU Access

| Provider | What you get | Notes / Limits |
|----------|--------------|----------------|
| Google Colab (free) | Hosted notebook, limited T4 | Session limits (~12h); quota fluctuates |
| Kaggle Notebooks | T4 ×2, ~30h/week | Phone verification; multi-GPU / TPU options |
| Hugging Face ZeroGPU | Shared RTX Pro 6000 Blackwell for Gradio Spaces | Short daily quota (minutes); demo-oriented |
| NVIDIA NIM / build.nvidia.com | Free endpoints for many open models (incl. recent DeepSeek, Nemotron) | OpenAI-compatible; no card for free tier |
| Groq free tier | Fast inference on supported models | Rate limits; no card |
| Google AI Studio / Gemini free | Flash models, limited daily | May train on data; no card |
| OpenRouter free | Limited free models / daily requests | Card-free options available |
| Cloudflare Workers AI | 10k neurons/day | Edge inference |
| Modal / Lightning AI | Free monthly compute / studios | Check current balances |
| NVIDIA Run:ai (open-sourced) | Full GPU orchestration platform (Apache 2.0) | Self-host; supply own K8s/GPUs |
| Startup programs (Together, Baseten, Fireworks, AWS, GCP, etc.) | Credit grants | Vary by stage |
| RunPod / Vast.ai | Cheap spot GPUs | Paid but lowest $/hr |

## Hosting & Serving

- **DeepInfer** (new open, Apache 2.0) — DeepSeek production stack for V4.1-Flash; high efficiency claims; dual NVIDIA/Huawei
- **vLLM / SGLang / llama.cpp / TensorRT-LLM** — primary stacks for large open MoEs (Beam, Muse Spark, DeepSeek, Nemotron, Ming-3.0); vLLM TorchTPU added
- **Hugging Face Spaces + Hub + Inference** — models, ZeroGPU demos, providers; TorchNeuron for Trainium
- **Diffusers + ComfyUI** — image pipelines (FLUX 3 Klein, Qwen-Image 2.1, Cosmos)
- Free LLM API directories (updated frequently)
- Voice agent SDKs (Mistral Voxtral 3 + LiveKit)

## Agent & Developer Tooling

- Agent harnesses optimized for recent Flash models (DeepSeek, MiniMax)
- Agent memory systems (e.g., Databricks Agent Bricks), MCP, tool-calling
- On-device / local agent stacks (Muse Glimmer, efficient MoEs)
- TRL for efficient post-training with fused LM head
- Accelerator backends: TorchNeuron (Trainium), TorchTPU, Huawei support via DeepInfer

## Developer Focus Areas (current)

- Evaluating and serving new efficient Flash/agent models (MiniMax M3.1, DeepSeek 1017) with open stacks like DeepInfer
- Voice/speech agents (Voxtral 3)
- Local/on-device agents (Muse Glimmer)
- Open audio/speech models (Ming-3.0)
- Leveraging free/NIM/serverless endpoints, non-NVIDIA accelerators (Trainium/TPU), Run:ai for self-hosted orchestration, and startup credits

---

*When a free tier changes or a tool is superseded, edit the existing row/bullet instead of appending a near-duplicate.*
