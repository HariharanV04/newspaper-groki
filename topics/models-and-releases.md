# Models & Releases

Living document. New entries go at the top. Older entries are refined or marked superseded rather than duplicated.

**Last refined:** 2026-11-04

---

## Frontier / Flagship & Large Open

### Mistral Large 4 (ML4 / “Le Chonk”) (weights Oct 29, 2026; high traction Nov 4)
- **Type:** Trillion-parameter open-weight flagship (Mistral). ~1T total / 49-52B active multimodal MoE (text+image), 1M context. Weights on Hugging Face + API.
- **Role:** Cybersecurity defense, advanced coding and agentic tasks. Claims ~47% fewer tokens than GLM-5.3 with comparable performance; improved Terminal-Bench 4.0 to ~41%. Tops open models on Coding Agent Index (vendor). Enables self-hosted control. Continued RL post-preview; trained on 3,800 Nvidia Grace Blackwell GPUs in Europe.
- **Status:** Open weights released. Fine-tuning support in TRL 1.17 (LoRA on single 8xB300 node keeping FP8). Dual-use acknowledged; continues high HF activity. Part of new multimodal generation with more models planned.

### Weight-Space Programming / GPT-6 Astra weight editing (MIT CSAIL, Nov 2, 2026)
- **Type:** Research demonstration (not a new model release). GPT-6 Astra used as editor of existing networks.
- **Role:** Shows frontier LLMs can inspect raw weights, diagnose failure modes (e.g., reasoning loops), and directly rewrite small percentages of parameters without gradients or training. Also identified trained behaviors from weights alone and wrote small policy networks from scratch.
- **Status:** Public report + full logs (MIT CSAIL). Key result: 0.016% edit to Qwen3.5-0.8B raised MATH-500 7.9%→48.1%, GSM8K 13.8%→67.1%, IFEval 21%→62.3%. Community interest high; reproduction efforts noted. Related HF demos circulating.

### Hydrogen-1.0 (Deep Principle, Nov 2, 2026)
- **Type:** 753B open-weight scientific MoE (MIT, ~40B active, 1M context). Post-trained from Z.ai GLM-5.3 on domain lab data (chemistry, materials science, life sciences) + discovery trajectories.
- **Role:** Scientific research assistant for formulating questions, designing experiments, and discovery in specialized domains. Self-reported edge over GPT-6 Astra on FrontierScience-Research (38.3% vs 33.3%).
- **Status:** Weights on Hugging Face (gated) and ModelScope; NVFP4/MXFP4 variants. API via NeuroSpark and Mira app. Full training data/recipe not released. Independent verification pending.

### LongCat-2.5 (Meituan, Nov 2, 2026)
- **Type:** Native multimodal 1.6T total / ~48B active MoE, 1M context.
- **Role:** Long-horizon agentic tasks (complex coding across codebases, full project builds, visual coding, creative design, 3D). Trained with large-scale agentic RL on long trajectories; optimized for Chinese domestic accelerators.
- **Status:** API live (OpenAI/Anthropic-compatible endpoints, limited-time low pricing ~$0.30/$1.20 per M tokens). Web chat available. GitHub and Hugging Face weights listed as coming soon. Strong self-reported scores on Terminal-Bench variants, BrowseComp, MCP Atlas, AutomationBench, etc.

### DeepSeek dsh-superagent v0.1.0 (open-sourced Nov 1, 2026)
- **Type:** MIT-licensed research-prototype coding agent (TypeScript bundle for DeepSeek Harness).
- **Role:** Proactive/local coding agent for a single GitHub repository. Router-worker design: turns user requests into Tickets and runs them in isolated worker sessions. Observes by default for proactive work.
- **Status:** Open on GitHub. Runs on user's machine (requires Node.js 22+, git, Python, tmux, GitHub CLI). Uses whatever model the Harness profile is set to. Early research prototype; real-world coding quality not fully measured.

### Nace AI Drex Max v1 27B (open weights Nov 1, 2026)
- **Type:** Dense 27B multimodal decision model (Open RAIL-M). Does not generate text; one forward pass returns probabilities over user-supplied options (up to 255). Supports text + images/screenshots.
- **Role:** Efficient decisions for computer-use agents, routing, classification, policy checks. Low latency/cost alternative to full generative models in agent loops. Strong self-reported scores on Decision Index (~67) and related benches.
- **Status:** Open weights (BF16, Q8_0 GGUF, affine Q4) + llama.cpp/Ollama/MLX forks. Runs on NVIDIA (8-bit ~26GB), Apple Silicon (24GB+ Q4), CPU. API also available. Ideal for local agent decision layers.

### Microsoft Mage-VL-Cowork 4B (Nov 1, 2026)
- **Type:** Hybrid 4B computer-use vision-language model.
- **Role:** Agentic computer use / cowork tasks.
- **Status:** Open release. Early community interest for cheaper agent computer-use.

### SenseTime SenseNova Loop-9B-Preview (recent)
- **Type:** 9B multimodal language model (looped decoder).
- **Role:** Long-context and agentic workflows (document understanding, coding, tools). Claimed to match larger models on selected benches.
- **Status:** Open-sourced. Unverified independent benches.

### Baseten joey-1 (Nov 1, 2026)
- **Type:** 2B decision model post-trained from Qwen3.5-2B (MIT).
- **Role:** Calibrated probability outputs for labels/decisions. Extremely low cost ($0.01/1M input on Baseten).
- **Status:** Weights on Hugging Face. Complements larger decision models like Drex Max.

### Google DeepMind Gemini 4 Carbon (Oct 28, 2026; limited access ongoing)
- **Type:** Closed frontier model, successor to Gemini 4 Argon. Google’s strongest to date.
- **Role:** Long-horizon agentic coding, cybersecurity defense (vulnerability finding/patching), multi-day autonomous workflows. Tops AA Intelligence Index v5.0 at 59. Strong on SEC-bench, ExploitGym, CWE-bench, Terminal-Bench, secure code gen.
- **Status:** Announced; limited access to cyber defenders via Fairwind Program. Broader rollout later. Intro pricing $2/$10 per M tokens (later $4/$20). No open weights. Engaged in US gov pre-release testing.

### NVIDIA Nemotron 3.5 Transcribe (ongoing, high HF activity Nov 4)
- **Type:** Open-weight speech model for intelligent transcription (30B-A4B).
- **Role:** Multilingual (40 langs) transcription, translation, speaker diarization/attribution, audio Q&A. Strong on open ASR leaderboards.
- **Status:** Weights on HF; active relevance for speech agents. Free NIM endpoints available. Trending.

### Liquid AI LFM3 family (Oct 27, 2026; top trending Nov 4)
- **Type:** Six open-weight ~2B models from shared LFM3-1.7B-Base backbone. Text (1.73B, 256K ctx), VL (video), Audio (speech in/out), Omni, and two decision models (typed outputs). Tri-hybrid architecture.
- **Role:** Local/edge agents, specialized fine-tuning, multimodal on-device. ~1 GB at 4-bit. Single-GPU fine-tune.
- **Status:** Weights + GGUF/MLX/ONNX/FP8 on HF. High activity (LFM3-1.7B top trending). Liquid reports strong agentic/local performance (self-reported). LFM Open License. WebGPU demos noted.

### OpenAI GPT-6.1 Terra (Oct 26, 2026)
- **Type:** Mid-tier closed model (1.05M context) optimized for visual reasoning and computer use.
- **Role:** High-volume everyday agentic work at half prior Terra price ($1/$5). Stronger Terminal-Bench, Agents’ Last Exam, lower errors, faster than higher-end siblings on many tasks (OpenAI figures).
- **Status:** Live in ChatGPT Work, Codex, and API (`gpt-6.1-terra`).

### Google DeepMind Genie 4 (Oct 27, 2026)
- **Type:** Real-time interactive world model with native audio generation.
- **Role:** Photorealistic simulations with real-time NL steering, better physics/humans, up to ~2 min consistency. For robotics training, creative pre-vis, gaming, etc.
- **Status:** Research preview (trusted testers). Expanding to Google AI Ultra (Project Genie) and early Gemini API partners.

### Pika H3 Flex (Oct 29, 2026)
- **Type:** Open-weight video model post-trained from MiniMax H3. ~33B-class image-to-video with audio. Weights on HF (Pika-Labs/Pika-H3-Flex).
- **Role:** Professional creative iteration: 6-step generation with synchronized stereo audio, up to 15s clips, multi-reference (up to 12), 5 exportable audio stems, draft-to-4K upscale. #1 open-weight on DesignArena t2v (Pika).
- **Status:** Open weights + GitHub inference + day-0 ComfyUI/Diffusers. API available (low per-second pricing). Local requires high-end GPU.

### Diffuspace Clover-35B-A3B-Preview (trending earlier Nov)
- **Type:** 35B-parameter MoE preview applying block diffusion to coding and tool-use.
- **Role:** Agents with block-diffusion architecture for coding/tool workloads.
- **Status:** Community evaluation ongoing.

### Nanbeige4.3-33B (Oct 24-25, 2026)
- **Type:** 33B dense transformer (Llama-style, 52 layers, GQA), Apache 2.0, 512K context, BF16 (~66GB). English/Chinese.
- **Role:** Flagship teacher for Nanbeige4.3 series; agentic coding and cowork tasks. Self-reported SOTA in ~30B open class on most agent/coding benches (e.g. Terminal-Bench 2.1 80.9, DeepSWE 65.5).
- **Status:** Weights + Base on HF. Transformers/SGLang/vLLM support (TP=4). Thinking default on. Quantizations appearing. Ongoing traction.

### Moonshot AI Kimi K3.1 Pro (Oct 23, 2026; weights due Nov 4)
- **Type:** 2.8T total / 104B active MoE, 1M context, multimodal (text+image).
- **Role:** Frontier-class coding, agentic, 3D/CAD, finance. Independent Intelligence Index 55 (4th). Strong Terminal-Bench and other agent scores. Cyber data filtered for open release.
- **Status:** API live ($2/$10). Open weights due Nov 4, 2026. Highspeed variant available. Large hardware needs.

### Microsoft Agensh (open-sourced Oct 24, 2026)
- **Type:** Decentralized multi-agent harness (MIT) for up to 1,024 self-organizing coding agents.
- **Role:** Scales agent organizations without central orchestrator; improves ProgramBench pass rates via concurrent self-assignment, shared Git/messaging/context.
- **Status:** Full code + reproduction guide open. Preprint arXiv:2609.26781.

### Hugging Face Carbon-X (Oct 22, 2026)
- **Type:** 14B multimodal (Qwen3-14B base) for DNA sequence analysis/generation + natural language.
- **Role:** Scientific tool for querying genomic effects, mutations, gene activity; local-runnable for privacy.
- **Status:** Open weights released. First-of-kind DNA chat model from HF.

### Recursive Flint (Oct 21-22, 2026)
- **Type:** 40B MoE (~2.5B active), Apache 2.0 coding model.
- **Role:** Local laptop coding agent (high tok/s on consumer hardware). Largely AI-developed via Eureka Machine.
- **Status:** Weights freely available. Strong for on-device/local use.

### MiniMax M3.1 Flash (API Oct 19; weights Oct 23, 2026)
- **Type:** Efficient Flash MoE (428B/23B active), 1M context, multimodal for agents/coding.
- **Role:** Low-cost high-performance agentic/coding ($0.15/$0.60). Day-0 vLLM/NeMo support.
- **Status:** Weights public. Continues strong relevance; note on hallucination tendencies.

### NVIDIA Nemotron 3.5 Bolt E4B 4GB (Oct 23, 2026)
- **Type:** Small open model (~8B/4B effective) post-trained from Gemma 4 E4B.
- **Role:** Local conversational agents, voice, NPCs, embedded. ~4GB VRAM, 64K context, multi-turn tools.
- **Status:** Open weights (BF16 + Q4 GGUF) on HF, Ollama, etc. OpenMDW-1.1.

### DeepSeek DeepInfer + V4.1-Flash (Open-source inference Oct 20; model Oct 17)
- **Type:** Production inference stack (DeepInfer, Apache 2.0) for DeepSeek-V4.1-Flash (multimodal MoE, 1M context, MIT weights).
- **Role:** High-throughput, low-latency serving. Dual NVIDIA / Huawei.
- **Status:** Framework on GitHub; model live. Ongoing relevance and high downloads. NVFP4 size-optimized variants for Blackwell. Top HF activity Nov 4.

### Other recent
- Qwen3.8 variants (esp. 27B high downloads), DeepSeek Flash updates, Kling 4.0, Canva image model, OlmoEarth, various decision and embedding models continue as notable.
- Unlimited-OCR-2 (Baidu), Qwen3.5-4B-3D-Coder, Cosmic Lightning 2B, LTX-2.5 video, SAM3, etc.
- OpenAI GPT-Rosalind-6 (biology model on GPT-6 Astra weights, recent report).
- JetBrains Mellum2.1 with MTP head for speculative decoding speedups.
- PrunaAI P-H3-Image: smaller/faster open image model derived from MiniMax-H3.

## Other / Infrastructure

- Kimi K3.1 Pro (open weights pending Nov 4)
- Carbon-X genomic model
- Flint local coding
- DeepInfer open inference
- Nemotron small models for local agents
- LFM3 family for multimodal edge
- Transformers ongoing support
- TRL, Diffusers updates (FLUX.3 Image Klein, Pika H3 Flex, multi-teacher distillation)
- Cisco Project Quarry (agent behavior detection, open-sourced Oct 28)
- POCKET-Darwin-180B CPU GGUF for high-end no-GPU inference
- FreeToken edge MoE serving runtime

---

*When a model is superseded or major details change, update the existing entry rather than adding a duplicate.*
