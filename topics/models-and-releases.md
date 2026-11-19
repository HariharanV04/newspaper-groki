# Models & Releases

Living document. New entries go at the top. Older entries are refined or marked superseded rather than duplicated.

**Last refined:** 2026-11-19

---

## New / Stabilizing Infrastructure (Nov 17-19)

### Google Gemini 4 Neon (Nov 18, 2026)
- **Type:** Closed mid-tier Gemini 4 model (adapted from Carbon). Multimodal (text/image/audio/video), 1M context, thinking levels low/medium/high/xhigh.
- **Role:** Frontier-level intelligence for complex coding, knowledge work, and science at higher speed and lower cost than top-end models.
- **Status:** API $3/$15 per M tokens (cached $0.15; batch/flex half). Live in Gemini API/AI Studio, Antigravity (Pro/Ultra), Gemini app, GitHub Copilot. Strong AA Index (~61 xhigh), Vals, Agent Arena rankings. No free tier.

### Microsoft MAI Code 2 / Code 2 Flash / Cyber 2 Flash et al. (Nov 17, 2026 Ignite)
- **Type:** Closed sparse MoE + vision coding/security/image/realtime models (1M+ context for coding).
- **Role:** Enterprise agentic coding and cyber at aggressive price-performance (claims Code 2 ~98% GPT-6.1 Sol at ~40% price; near Opus at fraction of cost).
- **Status:** Available in GitHub Copilot (various tiers); licensed weights for Azure customization. Decision models also GA.

### OpenAI GPT-6.2 Astra and Sol (Nov 17, 2026)
- **Type:** Closed frontier/everyday models. 1.05M context, text+image.
- **Role:** Cheaper agentic/coding and general work (Astra ~20% price cut; Sol everyday).
- **Status:** Live in ChatGPT Work, Codex, API, GitHub Copilot. Background-mode beta added.

### Tencent Hy4 flash (open weights Nov 17-18, 2026)
- **Type:** Open multimodal MoE (220-224B total / 12B active, incl. Engram), 1M context.
- **Role:** Cost-efficient multimodal and long-context work; now self-hostable.
- **Status:** Weights (base/FP8) on HF/ModelScope under Tencent Hy License. Prior ultra-cheap API ($0.07/$0.281). Available in WorkBuddy/Yuanbao.

### SenseTime SenseNova-Loop-9B (Nov 17, 2026)
- **Type:** Open Apache 2.0 ~9B multimodal (text/image). Looped architecture (32 physical layers → 56 executions via shared middle block + mHC).
- **Role:** Parameter-efficient depth for agents/coding/data analysis; competitive with Qwen3.8-27B on several benches.
- **Status:** Weights + code on HF/GitHub. 512K context; 4-bit ~4.9GB, low VRAM (~10GiB at 64K). Day-0 quant support.

### Reson8 Rumble-2-Flash (highlighted Nov 18)
- **Type:** Open 0.5B speech ASR (Apache 2.0), 40+ languages.
- **Role:** Efficient multilingual ASR matching much larger models on phone calls and HF Open ASR leaderboard.
- **Status:** Open weights on HF. Practical for edge/deploy balancing accuracy and throughput.

### Phancy Phai-A1 (Nov 18, 2026)
- **Type:** Open (Apache) fast coding/agent model post-trained from Qwen, 1M context.
- **Role:** PC/Huawei Ascend runnable agentic coding.
- **Status:** Open weights released.

## New / Stabilizing Infrastructure (Nov 16-17)

### Alibaba Qwen4-Max (Nov 16, 2026)
- **Type:** Closed flagship MoE (~2.4T total / 71B active + N-gram embeddings), native vision, 1M context.
- **Role:** Long-horizon agentic work, coding, professional tools, 3D/scientific discovery. Efficiency-focused (claims significant token/cost reductions vs Qwen3.8-Max).
- **Status:** API live on QwenCloud ($1.50/$4.50); available in Qwen Studio, QwenWork, Qoder. Smaller Qwen4 open weights planned. 1M free quota for 90 days on some plans.

### Tencent Hy4 flash (API Nov 16; weights later)
- **Type:** Closed then open low-cost multimodal MoE (224B total incl. Engram / 12B active), 1M context.
- **Role:** Cost-efficient multimodal and long-context work.
- **Status:** API live at $0.07 input / $0.281 output per M tokens on TokenHub. Weights now open (see above).

### Meituan LongCat-Video-Avatar 1.6 (Nov 15, 2026)
- **Type:** Open-weight (MIT) audio-driven human video generation.
- **Role:** Improved lip sync, facial/body expressiveness, and long-video consistency (>10 min videos).
- **Status:** Weights + technical report on Hugging Face / ModelScope. Strong internal preference rankings.

*Note: Full historical entries remain below this refined top section. Older items are retained for continuity and marked as ongoing where still relevant. See git history for complete prior content.*
