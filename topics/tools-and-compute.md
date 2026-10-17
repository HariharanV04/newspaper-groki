# Tools & Compute

Living reference for free/low-cost GPUs, hosting, inference stacks, and developer tooling. Quotas and offerings change; update entries in place.

**Last refined:** 2026-10-17

---

## Free / Low-Cost GPU Access

| Provider | What you get | Notes / Limits |
|----------|--------------|----------------|
| Google Colab (free) | Hosted notebook, limited T4 | Session limits (~12h); quota fluctuates |
| Kaggle Notebooks | T4 ×2, ~30h/week | Phone verification; multi-GPU option |
| Hugging Face ZeroGPU | Shared RTX Pro 6000 Blackwell for Gradio Spaces | Short daily quota (minutes); demo-oriented |
| Lightning AI free plan | Persistent studios + credits | Better persistence |
| NVIDIA NIM / build.nvidia.com | Free endpoints for many open models | OpenAI-compatible; no card for free tier |
| Inference.net | Grants up to $10k free compute | For open-source AI projects; application |
| Modal | Free monthly compute credits | Check current balances |
| Startup programs (AWS, Google Cloud, MSFT, Anthropic, OpenAI, Together, etc.) | Large credit grants | Vary by stage; partner routes common |
| RunPod / Vast.ai | Cheap spot GPUs | Paid but lowest $/hr for real work |
| Leafcloud | Free Blackwell tier (coming) | 50 GPU hours/month waitlist; EU |
| Oracle Always Free | Always-on ARM CPU | Lighter inference |

## Hosting & Serving

- **Hugging Face Spaces + Hub + Inference Providers** — models, datasets, ZeroGPU demos, free/PRO credits
- **vLLM / SGLang / llama.cpp / TensorRT-LLM** — primary open serving stacks
- **Diffusers + ComfyUI** — image/video pipelines (Qwen-Image, LTX, Flux variants)
- **NVIDIA Run:ai** (open-source) — K8s GPU orchestration
- Free LLM API directories and live ranking sites (updated daily)

## Agent & Developer Tooling

- Agent memory systems (TencentDB and others), MCP clients, tool-calling harnesses
- Decision-model serving (explicit choices + probabilities)
- TRL / Transformers updates for longer training sequences and new models (Beam)
- On-device / local agent stacks (efficient MoEs)

## Developer Focus Areas (current)

- Running large open frontier models (Beam, Muse Spark, Nemotron) vs efficient local MoEs
- Long-context multimodal and agent pipelines
- Fast image/video generation
- Persistent memory and reliable decision outputs
- Leveraging free/startup GPU credits and serverless endpoints

---

*When a free tier changes or a tool is superseded, edit the existing row/bullet instead of appending a near-duplicate.*
