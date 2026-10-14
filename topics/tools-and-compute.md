# Tools & Compute

Living reference for free/low-cost GPUs, hosting, inference stacks, and developer tooling. Quotas and offerings change; update entries in place.

**Last refined:** 2026-10-14

---

## Free / Low-Cost GPU Access

| Provider | What you get | Notes / Limits |
|----------|--------------|----------------|
| Google Colab (free) | Hosted notebook, limited T4 | Session limits (~12h); quota can fluctuate |
| Kaggle Notebooks | T4 ×2, ~30h/week | Phone verification; good multi-GPU free option |
| Hugging Face ZeroGPU | Shared high-end GPU for Gradio Spaces | Short daily quota; demo-oriented |
| Lightning AI free plan | Persistent studios + monthly GPU hours | Better persistence than pure notebooks |
| NVIDIA Developer free endpoints | Many large open-weight models via OpenAI-compatible API | build.nvidia.com; no card required for free-tier models |
| Modal / Replicate | Free credits / tiers | Check current credit balances |
| Oracle Always Free | Always-on ARM CPU instances | Useful for lighter inference / always-on services |
| RunPod / Vast.ai | Cheap spot GPUs | Paid but often the lowest $/hour for real training |

## Hosting & Serving

- **Hugging Face Spaces + Hub** — free public models/datasets; CPU Spaces; ZeroGPU for demos
- **vLLM / SGLang / llama.cpp / TensorRT-LLM** — primary open serving stacks
- **Diffusers + ComfyUI** — image generation/editing pipelines (including Qwen-Image-2.1-Turbo)
- **NVIDIA Run:ai** (now open-source) — Kubernetes-native GPU scheduling and fair-share for clusters

## Agent & Memory Tooling

- **TencentDB Agent Memory** (MIT) — local SQLite default + team-level memory hub
- Broader ecosystem of MCP clients, tool-calling harnesses, and agent orchestration frameworks continues to expand

## Developer Focus Areas (current)

- On-device / local agents (efficient MoEs)
- Long-context multimodal pipelines
- Fast image generation (8-step Turbo-style checkpoints)
- Persistent agent memory and recovery

---

*When a free tier changes or a tool is superseded, edit the existing row/bullet instead of appending a near-duplicate.*