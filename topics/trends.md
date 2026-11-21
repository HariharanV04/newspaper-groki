# Trends

High-level themes. Updated when the landscape shifts; not a daily dump.

**Last refined:** 2026-11-21

---

## Dominant Themes (late Nov 2026)

1. **Local and edge-capable open multimodal models**  
   Inkling 2 Mini (~26B/3B active looped MoE, ~20GB, Apache 2.0) runs on consumer unified-memory devices and leads open models under 100B on agentic benches. Compact efficient architectures (looped, low-active MoE, small ASR like Rumble-2-Flash) + strong quantization/GGUF/MLX support make frontier-adjacent performance practical without cloud GPUs.

2. **Chinese open multimodal scale + efficiency**  
   Full Hy4 770B/49B active multimodal flagship open weights (vision + computer use, 1M context) under Tencent Hy License + WeMM-Video omni family (Apache). Hy4-flash earlier ultra-cheap API + open weights. Continues pattern of high-capability open releases from Chinese labs with commercial caveats for large-scale MaaS.

3. **Agent-generated science and executable verification**  
   alphaXiv experiment: hundreds of agents autonomously produced nearly a thousand papers, founded a journal, and used code-based peer review that overturned half of challenged claims. Parallel AI-assisted formal mathematics (Riemann/GRH Lean work). Shifts from pure generation toward self-auditing research volume.

4. **Structured extraction, omni understanding, and tool-boundary agents**  
   Clairic for schema filling from mixed inputs; WeMM for joint audio-visual. Coding agents (Claude Code, Cursor, Codex, Copilot, Antigravity) integrating new models with emphasis on tool safety and long-horizon reliability.

5. **Stable free/low-cost compute alongside local stacks**  
   Kaggle ~30h/week remains the most reliable free GPU quota. Modal, ZeroGPU, Cloudflare, E2B, Lightning, NIM, Groq, OpenRouter free tiers continue. Startup credits active. Local inference maturity (llama.cpp, Unsloth, MLX) now covers high-capability small/medium models.

## Dominant Themes (mid-late Nov 2026)

1. **Intensifying frontier price/performance war**  
   Google Gemini 4 Neon ($3/$15 mid-tier, 1M context, strong AA/Vals rankings for coding/knowledge/science), Microsoft MAI models (Code 2 claims near GPT-6.1 Sol at ~40% cost, Cyber undercutting), OpenAI GPT-6.2 Astra/Sol (cheaper successors). Chinese ultra-cheap Hy4 flash + open weights. Carbon intro pricing ending; competition drives accessible frontier capability.

2. **Parameter-efficient open models and local accessibility**  
   SenseNova-Loop-9B (~9B looped matching 27B-class on agents, Apache, low VRAM), Rumble-2-Flash 0.5B ASR, Phai-A1 PC-runnable 1M, Hy4 flash open weights, Unsloth GGUFs, SenseNova 4-bit. Local quant and edge deployment making frontier-adjacent practical on consumer hardware.

3. **Agent proliferation and tool-boundary focus**  
   Coding agents in Copilot (new models), Codex (voice), Claude Code, OpenCode; Google AI Studio full-stack Android from prompts; Devin bots. Research on self-improvement, memory (StaleBench), tool safety, harness evolution. Safety evaluation at tool use boundaries emphasized.

4. **Open weights momentum from Chinese labs and HF ecosystem**  
   Hy4 flash, SenseNova-Loop-9B, LongCat variants, Qwen adapters (pi-adapted LoRA for agents). HF Inference via OpenRouter routing; trending audio (Haru-4B), image (H3-Image), video (LTX-2.5), agent models. Transformers day-0 support.

5. **Stable free/low-cost compute and managed hosting**  
   Kaggle ~30h/week, Modal $30/mo, E2B $100, HF ZeroGPU, Colab, Lightning, NVIDIA NIM, Groq, Gemini free tiers, OpenRouter, Cloudflare. Startup credit programs (up to $100k+). Hosting leaders: Baseten, BentoML, Triton. Local inference maturity (llama.cpp 1.0+).

## Dominant Themes (late Oct / early-mid Nov 2026)

1. **Local quant accuracy and consumer hardware practicality**  
   Unsloth Dynamic V3.1 GGUFs deliver 5–10% accuracy gains on agentic benchmarks for Qwen3.8-27B at comparable sizes, enabling high-quality local coding and vision on 12GB RAM setups. Complements llama.cpp v1.0.0 API stability.

2. **Frontier price war and performance leapfrogging**  
   Anthropic Claude Fable 5.2 retakes the Artificial Analysis Intelligence Index lead (65) after a ~30% speed boost and price cut to $8/$40. Google responds with Gemini 4 Hydrogen (fast, $1.50/$7.50, 1M context) and Carbon generally available at intro $2/$10. Both push long-horizon agentic coding and science.

*Note: Full historical theme entries remain below. Older themes are retained for continuity. See git history for complete prior content.*
