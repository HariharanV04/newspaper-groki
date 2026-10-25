# Current AI Briefing

**Last updated:** 2026-10-25

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### Microsoft Agensh open-sourced (Oct 24, 2026)
- Decentralized multi-agent harness that scales to 1,024 agents without a central orchestrator. Agents self-organize via shared Git workspace, messaging, and context board.
- On ProgramBench (hardest tasks, offline, 6h budget): mean test-pass rate rises from 19.31% (1 agent) to 28.78% (128 agents) with GPT-5.6-sol; pandoc from 33.89% to 55.06% at 1,024 agents. Roles emerge organically. With GPT-6.1-sol, pandoc reaches 79.59% at 32 agents.
- MIT licensed. Includes Docker Compose setup, reproduction guide. Code: github.com/microsoft/Agensh. Preprint (arXiv:2609.26781) from Sep 2026 now with full open code.

### Block Dessa (announced Oct 23, 2026)
- Full-duplex speech-to-speech model trained from scratch solely on human conversation audio (no text, no pretrained models). Listens and speaks simultaneously; handles interruptions, backchannels, emotion, sarcasm.
- Trained on one NVIDIA GB200 NVL72. Runs locally on MacBook Pro M4 Max or better, faster than real-time. Research preview: waitlist + early access for AI safety researchers. No weights/API yet.
- From small lab at Block (Jack Dorsey). Claims first realistic live conversation model trained only on speech.

### Ongoing / recent major
- Moonshot Kimi K3.1 Pro (Oct 23): 2.8T/104B MoE, 1M context, multimodal. AA Index ~55 (near top open-to-be). API $2/$10; open weights by Nov 4. Strong coding/3D/finance; cyber data filtered for open release.
- NVIDIA Nemotron 3.5 Bolt E4B 4GB (Oct 23): open small (~8B/4B effective) for local agents/NPCs/voice. ~4GB VRAM target, 64K context. On HF/Ollama.
- MiniMax M3.1 Flash weights public (428B/23B MoE, low-cost agents). Diffusers 0.42.0 (FLUX.3 Image Klein with layout control, Fibo 2.0, Kandinsky 6, etc.).
- Carbon-X (HF DNA chat), Recursive Flint (laptop coding MoE), DeepSeek V4.1 Flash + DeepInfer, Beam, Muse series continue relevant.

## Hugging Face & Ecosystem Updates
- Diffusers 0.42.0 (Oct 23): FLUX.3 Image Klein (text-to-image + multi-ref edit + bounding-box layout control), Bria Fibo 2.0, Kandinsky 6 (video+audio), SANA-WM, RFD4-Proteína. Python 3.11+ required. Modular pipelines, LoRA, hardware (TorchTPU).
- Nemotron Bolt E4B, MiniMax M3.1 Flash, various Qwen3 coder variants trending/updated on HF.
- Papers: Foundation4D (NVIDIA unified AV perception), Cola2 (hierarchical LM), FrontierCS 2 (agent CS R&D bench); WildAWM for computer-use agent environments.

## Research (recent arXiv ~Oct 24-25 focus)
- Agensh preprint confirmed with open code; OverSeer multi-agent world models; Agentic World Action Models; Self-Improving Agents with World Model Predictive Paths.
- Ongoing: agent safety (EpiSEM-Bench missing evidence), test-time reasoning pruning, sycophancy/deference, control evals, hierarchical generation (Cola2), AV foundation models, speech-native training (Dessa).
- Themes: multi-agent scaling without orchestrators (Agensh), speech-only training (Dessa), efficiency in agents/world models, evaluation of open-ended R&D, synthetic computer-use environments.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (stable late Oct 2026):**
- Google Colab (T4, session limits), Kaggle Notebooks (~30h/week T4x2), Hugging Face ZeroGPU (shared high-end for Spaces, minutes/day)
- NVIDIA NIM free endpoints, Groq, Google AI Studio, OpenRouter rotating free, Cloudflare Workers AI
- Lightning/Modal free credits; NVIDIA Run:ai fully open-sourced (Apache 2.0) for self-hosted K8s GPU orchestration
- Startup grants; low-cost spots (RunPod/Vast.ai)

**Hosting & tools:**
- Ollama/llama.cpp/Unsloth for local (Bolt E4B, Flint)
- vLLM/SGLang for MoEs (MiniMax, upcoming Kimi, DeepSeek, Nemotron)
- HF Hub/Spaces, Diffusers 0.42.0 for image/video
- Agensh for multi-agent coding experiments; voice research (Dessa waitlist)

## Trending Themes
- Multi-agent scaling without central orchestrators (Agensh open-source)
- Speech-native models bypassing text (Dessa)
- Near-frontier open weights imminent (Kimi K3.1 Pro Nov 4)
- Efficient local agents (Nemotron Bolt E4B) and low-cost Flash MoEs
- Specialized tools (Carbon-X genomics) and generative pipelines (FLUX.3 etc.)
- Free compute and open inference stacks enabling broad experimentation

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor changelogs, arXiv, GitHub). Vendor scores are not independent.*
