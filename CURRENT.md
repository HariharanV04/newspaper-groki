# Current AI Briefing

**Last updated:** 2026-11-11

This file is always overwritten with the latest full snapshot. For history and refined topic tracking, see `topics/` and `archive/`.

---

## Major Frontier & Open Model Releases (Past 24h focus)

### New / notable in past ~24-48h (Nov 9-11)
- **Anthropic Claude Fable 5.2 & Mythos 5.2** (Nov 9): Same underlying model. Outputs ~30% faster than 5.1; priced at $8 input / $40 output per M tokens (down from $10/$50). Optional fast mode 2.5x speed at double price. Tops Artificial Analysis Intelligence Index at 65 (max effort) ahead of Gemini 4 Carbon (60). Strong on FrontierSWE v2 (69.9%), Terminal-Bench-Science 0.1 (74.6%), OSWorld, coding, science. Pre-release demos: 1,000 agents formalized Fermat’s Last Theorem in 30 hours; designed three working electronic devices; solved open black-hole physics problems. Fable generally available with cyber/bio safeguards; Mythos 5.2 reserved for vetted Life Sciences / Cyber Verification programs (fewer safeguards). 1M context, 128K max output. Available on AWS, Google Cloud, Microsoft Foundry, Anthropic API.
- **Google Gemini 4 Carbon** (generally available Nov 10): Google’s strongest Gemini 4 model. Intro API pricing $2/$10 per M tokens through Nov 30, then $4/$20. 1M context. Strong agentic/cybersecurity and long-horizon work. Slightly trails Fable 5.2 on most published coding/science benches but cheaper and competitive on AutomationBench. AlphaProof Code agents formally verified security properties (forward secrecy, post-compromise security, authentication) of Signal’s real AArch64 libsignal code in four weeks. Rolling out to paid Gemini API, AI Ultra, business; not yet free tier.
- **Meta Muse Ember** (Nov 9): Smallest/cheapest Muse model for high-volume agent subtasks (tool calling, coding subtasks, routing, extraction, long-document parsing). $0.10 input / $0.50 output per M tokens (matches Haiku 5.5 / GPT-6 Luna tier; higher above 200K). 1M context, native text/image/audio/video. Strong on Terminal-Bench 4.0 vs Haiku (vendor).
- **Meituan LongCat-2.5** (weights published Nov 9, MIT): 1.6T total / ~48B active multimodal MoE. Accepts screenshots/video. Strong self-reported Terminal-Bench scores. Full weights on Hugging Face; no major inference providers yet.
- **Baidu ERNIE-5.5-Flash-Preview & ERNIE-Light-DT-1.0**: Listed on OpenRouter.
- **xAI Grok 4.8**: Finished pre-training after full stack rewrite in C; entered reinforcement learning.
- **NVIDIA GR00T 2**: Open world-action model (on Cosmos) for robotics. Predicts frames + actions. 71% average success with one demo/task, 95% with five; 40/50 tasks completed with zero demos. 100k hours of human first-person video available.
- **Anthropic workspace features** (Nov 10-11): Claude Whiteboards and Sheets in beta; Claude Data (Dashboards) generally available on paid plans.
- **OpenAI**: Businesses in ChatGPT (profiles, mention/click analytics, agents); Control Room for internal research inference tracking.

### Ongoing traction & recent
- Kimi K3.1 Pro continues high HF activity (2.8T multimodal MoE).
- Ripple-65B Preview, Qwen3.8-27B, LTX-2.5, MiniMax-H3-Image, various uncensored DeepSeek/Qwen GGUFs trending.
- Mistral Large 4 still efficient open flagship.
- NVIDIA Cosmos 3 open world models active on HF.

## Hugging Face & Ecosystem Updates
- Trending (as of Nov 11): speridlabs/idol (image-to-3D), xtools-at/DeepSeek-V4-Pro-Qwen3.5-9B-UNCENSORED-heretic, moonshotai/Kimi-K3.1-Pro, ricursiveAI/Ripple-65B-Preview, MiniMaxAI/MiniMax-H3-Image, Lightricks/LTX-2.5, NousResearch/Arete-27B, Qwen/Qwen3.8-27B, ccore/Qwen3.5-4B-3D-Coder, various Turbo/Heretic uncensored GGUFs.
- Recent HF updates: NVIDIA Nemotron 3.5 Transcribe / Cosmos 3 models; Qwen3.8-27B refreshed; many 3D-Coder and agent variants.
- Ecosystem: Continued day-0 Transformers/vLLM/SGLang support for new releases. SafetyPulse and other fine-tuning monitoring tools noted.

## Research (recent arXiv / HF Papers ~Nov 9-11 focus)
- AlphaProof Code (DeepMind): Agents wrote millions of lines of Lean proofs to formally verify Signal protocol security properties on real machine code.
- World models / robotics: GR00T 2, Gemini Robotics 2.5, World In-Context Learning for Agentic Robot Manipulation, SWAM (Scaling World Action Models).
- Agents: ExRL (sample-efficient long-chunk policy adaptation), Infrathon (long-horizon AI infra optimization), ReTrace (distilling tool-using agents), multi-agent frameworks for literature review and scientific discovery (Sage-Taiyi, Scientist World follow-ons).
- Other: MiniMax H3-Image (4K generation), dNaViT discrete visual codes, PhysOPSD physically plausible video, FraudBench (AI deception evaluation), Contrastive Discovery (open-ended scientific discovery).
- Themes: Formal verification with agents, world-action models for robotics, efficient agent distillation and long-horizon reliability, multimodal generation scaling.

## Free GPUs, Hosting & Developer Tools
**Free / low-cost compute (as of Nov 11 2026):**
- Kaggle: ~30 GPU hours/week (T4x2 or P100, 12h sessions).
- Google Colab free: limited GPU access, 12h max.
- Lightning AI: up to ~30 credits (~50+ GPU hours on T4) + free Studio.
- Hugging Face ZeroGPU: shared RTX Pro 6000 Blackwell, ~5 min/day for Spaces demos.
- Modal: $30 free compute/month + startup credits.
- NVIDIA NIM free endpoints, Groq, Google AI Studio (Flash family), OpenRouter free models, Cloudflare Workers AI (10k neurons/day), SambaNova free until card linked.
- New/notable: AMD Developer Cloud $100 credit on MI300X (approved); IteraCompute free Auto route (up to 30M tokens/month on open models); MangoBoost $10 signup + discount; various startup MaaS credits.
- Local: Ollama, llama.cpp (FP8/GGUF), vLLM/SGLang, MLX, FreeToken for MoE pooling.

**Hosting & tools:**
- Open weights: LongCat-2.5 (MIT, large), Kimi K3.1 Pro, Ripple-65B, Mistral Large 4, Arete-27B, MiniMax-H3-Image available for self-host or endpoints.
- Coding agents: Claude Code, Cursor, Codex, Copilot, Antigravity, Cline remain dominant. Anthropic workspace (Whiteboards/Sheets/Data) expanding Claude into collaboration tools.
- Inference: Day-0 support for new models; price competition (Carbon intro $2/$10 vs Fable $8/$40) lowering barriers.
- Video/image: LTX-2.5, MiniMax-H3-Image, GR00T 2 / Cosmos for robotics simulation.

## Trending Themes
- Price war at the frontier: Gemini 4 Carbon undercuts Fable 5.2 by ~4x on intro pricing while remaining competitive; Fable retakes AA Intelligence Index lead.
- Agent capabilities jumping: multi-agent formal math proofs, electronic device design, formal protocol verification, robotics world-action models with few-shot demos.
- Open-weight giants continuing (Kimi, LongCat now fully open, Mistral Large 4) alongside specialized small agent models (Muse Ember).
- Workspace and business integration: Claude adding Whiteboards/Sheets/Data; OpenAI Businesses profiles and analytics.
- Accessible free/local compute and coding agents remain foundational; HF trending dominated by image-to-3D, uncensored variants, video, and strong open MoEs.

---
*Always verify latest benchmarks, pricing, VRAM needs, licenses, and availability on official sources (HF model cards, vendor blogs, arXiv, GitHub). Vendor-reported scores are not independent. Caution on unauthenticated claims and gated releases. For cyber/specialized models, access is often restricted.*
