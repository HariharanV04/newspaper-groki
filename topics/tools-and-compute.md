# Tools & Compute

Living reference for free/low-cost GPUs, hosting, inference stacks, and developer tooling. Quotas and offerings change; update entries in place.

**Last refined:** 2026-10-18

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
| Startup programs (Together, Baseten, Fireworks, AWS, GCP, etc.) | Credit grants | Vary by stage |
| RunPod / Vast.ai | Cheap spot GPUs | Paid but lowest $/hr |

## Hosting & Serving

- **Hugging Face Spaces + Hub + Inference** — models, ZeroGPU demos, providers
- **vLLM / SGLang / llama.cpp / TensorRT-LLM** — primary stacks for large open MoEs (Beam, Muse Spark, DeepSeek, Nemotron)
- **Diffusers + ComfyUI** — image pipelines (FLUX 3 Klein, Qwen-Image)
- Free LLM API directories (updated frequently)

## Agent & Developer Tooling

- DeepSeek Harness updates for V4.1-Flash-1017
- Agent memory systems, MCP, tool-calling harnesses
- Decision-model serving patterns
- On-device / local agent stacks (efficient MoEs)

## Developer Focus Areas (current)

- Running and quantizing large open models (DeepSeek 1017, Beam, Muse Spark Open, Nemotron)
- Agentic coding and long-context pipelines
- Fast open image generation
- Leveraging free/NIM/serverless endpoints and startup credits

---

*When a free tier changes or a tool is superseded, edit the existing row/bullet instead of appending a near-duplicate.*
