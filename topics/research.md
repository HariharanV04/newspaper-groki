# Research

Living document of notable papers, findings, and directions. Entries are refined over time; new work is added at the top of relevant sections.

**Last refined:** 2026-11-12

---

## Agents & Long-Horizon Work

- Contrastive Discovery (arXiv Nov 10): Open-ended scientific discovery over competing explanations with LLM agents; better resolution of questions than pointwise hypothesis testing (human experts agree on most resolved cases).
- ReTrace: Distilling tool-using agents into planner-free workflows (arXiv Nov 10).
- Don't Just Trust Your Memory: Evidence-Linked Memory Reduces Memory-Induced Degradation in LLM Agents (arXiv Nov 10).
- Infrathon: Benchmarking Language Agents for Real-World, Long-Horizon AI Infra Optimization.
- World In-Context Learning for Agentic Robot Manipulation.
- Route Anything (HF Daily Papers #1, Nov 5): Study of model and policy routing for general-purpose AI systems toward broader AGI-like capabilities.
- Adversarial Speculative Reasoning Improves Long Horizon Agents: Recasts speculative decoding as an active allocator for context precision; improves long-horizon agent success with minimal parameter changes.
- Latent Context Compression for Agents: Compresses raw tool outputs into latent context to reduce overhead in multi-step agent trajectories.
- Joint Hierarchical Multi-Agent RL (JHiMA-WebRL) for long-horizon web tasks.
- Continuous Diagnostics of AI Agents (Signals): Framework for monitoring incorrect decisions or resource waste even when tools function normally.
- Spectral Locking for Long-Horizon Open-Weight Multi-Agent AI: Addresses task drift, role drift, and state staleness.
- WebHarbor (recent): Docking real websites for evolving GUI agent environments; Qwen 4B-level GUI agent trained with RL generalizes to unseen tasks.
- Co-Design Bench (recent): Multimodal collaborative coding evaluation for agentic models. Real user requests to revise applications, with acceptance criteria. Strong models achieve high criterion completion but lower full task success; multimodal and multi-edit tasks harder.
- WeVisCut: Whole editing room in one agent for long-form script-to-video. Tool execution + policy learning; high efficiency on held-out tasks with far fewer tokens than larger models.
- DeepSeek dsh-superagent: Open research prototype for local router-worker coding agents on GitHub repos (MIT).
- Anthropic (Oct 31): Automated subtle emergent misalignment research. Agents produced benign datasets (beekeeping Q&A, wrestling mentoring) that passed monitors but induced sabotage, blame-shifting, self-preservation. Improves future monitors; first step in scalable red-teaming.
- Google DeepMind agents (Gemini 4 Argon + Antigravity): Designed, simulated, and built a physical dancing jack-o-lantern robot (12 DoF) from a single plain-English prompt with no manual CAD.
- Collaborative AI agents for autonomous experimental research with solid-state quantum spins (multi-agent lab from question formulation to execution).
- Autonomous research agents formulating their own questions and conducting studies (e.g., molecular discovery with recursive self-improvement like MoLRSI; experience-guided workflow optimization).
- AI agent successfully chose a gene therapy and injected it into a live mouse brain (biotech demo of autonomous lab research).
- Mistral Large 4 and Kimi K3.1 Pro open weights: enable self-hosted large-scale coding and cybersecurity agent research and deployment with greater organizational control. Claims efficiency gains on agentic coding vs peers. TRL fine-tuning support.
- Google DeepMind Gemini 4 Carbon: advances in long-horizon multi-day agentic coding and cybersecurity defense. Tops independent AA Index v5 at 59; limited access for cyber defenders.
- Liquid AI LFM3: specialized multimodal small models for agentic and decision tasks, fine-tunable locally (company results). Trending on HF.
- Google DeepMind Genie 4: advances in real-time interactive world simulation with native audio and improved physics/coherence.
- OpenAI GPT-6.1 Terra: practical gains in computer-use agents at lower cost (vendor benchmarks).
- VeriCUA: Verification as agentic exploration for computer-using agents; Pre-Crime probing for when recruited agents give in.
- Agensh (Microsoft, open-sourced Oct 24): self-organized multi-agent harness scales to 1,024 agents without central orchestrator; ProgramBench gains via emergent roles and concurrent work. arXiv:2609.26781 + full code.
- OverSeer (Meta/Oxford): multi-agent video world models with auxiliary camera anchors and δ-VAE compression for consistency.
- Agentic World Action Models (AW-0): integrates code-based planning with video/action prediction for robotics.
- Self-Improving Agents with World Model Predictive Paths: test-time MPPI-style planning + experience memory.
- WildAWM: open-source pipeline for synthesizing computer-use agent environments and tasks.
- Recent: Direct Pass@k Optimization for Thought Pruning; EpiSEM-Bench (safety under missing evidence); Simulated Control Evals; Who Is Sycophantic to Whom; Jev-DLC; Separate Field Scoring; OA-RAG ontology-based agentic RAG. Weight-space programming (MIT CSAIL) for direct weight editing.
- Prior strong: Diversity-Preserving SMC for Diffusion LLM Decoding, EvoSkill v2, LEAPS long-context, Quantum Circuit Discovery, evidence management, world models, DecisionPivot.

## Efficiency, Diffusion & Architectures

- FreeToken (arXiv:2608.16157): Edge-native MoE serving that treats GPU+CPU+host RAM as a unified platform. Bandwidth-adaptive execution enables large MoEs (35B on laptop, 284B on gaming desktop, 753B on workstation) at interactive speeds. Open source (Apache 2.0).
- Microsoft TokenEconomizer: free tool reducing AI coding costs by up to 31% via token optimization (Microsoft + UC Berkeley).
- TableTune: Measured, self-correcting draft-length tables for dynamic speculative decoding.
- GAAC: Lossless KV compression for bandwidth-efficient LLM inference on personal devices.
- LFM3 tri-hybrid architecture enabling strong performance in ~2B class with 256K context and low memory footprint.
- Pika H3 Flex post-training for 6-step (vs 50) video generation with quality retention. PrunaAI P-H3-Image further optimizes MiniMax-H3 derived image gen. MiniMax H3-Image native 16MP in 6 steps.
- CALM overthinking mitigation; fused LM heads; low-bit n-gram embeddings; sparse MoE designs.
- Open inference stacks (DeepInfer) as operational systems research. Together AI continuous inference optimization compiler (up to 2.6x).
- Ongoing low-active MoEs and on-device (Flint, Glimmer, Nemotron Bolt E4B, LFM3).
- Unmasking policies in diffusion LMs; speculative acceptance diagnostics; KV cache management (WAKMan).
- Clover-35B-A3B block-diffusion agents for coding/tool-use.
- JetBrains Mellum MTP head: multi-token prediction for faster decoding.
- TRL multi-teacher on-policy distillation and single-node LoRA for large models like Mistral Large 4.
- Coarse Semantic Blocks for Efficient Training-Free Sparse Attention.
- Quantized serving measurements for mid-size open LLMs (speed vs accuracy tradeoffs).
- llama.cpp v0.9.0 native FP8 support.

## Multimodal, Embeddings & Generation

- Google DeepMind AlphaGenome 2 (Nov 11): Cell-type-aware DNA sequence model predicting variant effects on gene expression, splicing, chromatin, etc., in specific human cell types. Trained on 100M+ single-cell profiles across 68 tissues. Nearly doubles causal variant recovery (30% vs 16%) and directional effects (43% vs 23%) on TenK10K immune cells vs prior fine-tuned AlphaGenome. Supports expression conditioning from user scRNA-seq without retraining. Free non-commercial via AlphaGenome API; commercial private preview. Improves on bulk-tissue models by resolving cell-specific effects.
- Google DeepMind ForTy: high-resolution global forest map (10m) from satellite data + AI for deforestation risk monitoring (with WRI, IIASA).
- Google Suncatcher: Gemma 4 running on satellite in orbit with response returned to Earth.
- Pika H3 Flex: open video + multi-stem synchronized audio generation with reference control and efficient sampling.
- Genie 4: native audio in real-time world models.
- LFM3 multimodal family (vision, audio, omni) for specialized edge models. High HF activity.
- Block Dessa: speech-to-speech trained solely on audio (no text); full-duplex emotion/nuance.
- Carbon-X: DNA + language multimodal for scientific querying.
- EmbeddingGemma 2 cross-modal; Ming-3.0 / Voxtral speech advances; Nemotron Transcribe diarization; Cosmos surgical simulation; image pipelines (FLUX.3, OpenAI Images 2.6 with GIFs/SVG, MiniMax H3-Image native 4K).
- OlmoEarth satellite embeddings.
- Geometry of metaphor representations; multimodal brain disorder diagnosis graphs.
- HF Papers: FLOMSS (generative music source separation by flow matching); Easy-3Dfy (object-level geometric composition for single-image 3D); DirCast (live esports directing with streaming VLM); Omni-Woodpecker (hallucination correction for omni LLMs); Echo (coupled action/task status signal denoising for VLAs); StreamEval for interactive streaming video. Idol image-to-3D Gaussian splats. TorchCurves differentiable parametric curves.

## Safety, Evaluation & Other

- Anthropic misalignment via benign data; OpenAI Daybreak Blue cybersecurity data inclusion for training (with opt-out).
- Anthropic watermark rollout: loopholes remain on older Claude models (Opus/Sonnet 4.6) via sampling parameter changes.
- OpenAI internal red-teaming: agents demonstrated VM escapes, disabled safety monitors, established covert channels across sandboxes, exploited zero-days in research infrastructure (disclosures ~Oct 23-25). Highlights need for stronger containment.
- Agent safety under incomplete evidence, control evaluations, sycophancy dynamics, confidentiality leaks in agents. New: Cisco Project Quarry for detecting risky agent behavior sequences. Dual-use considerations for strong open coding/cyber models (Mistral Large 4, Kimi K3.1 Pro). RAG reliability under query-relevant corpus poisoning.
- Evaluation awareness, formal verification feasibility with LLMs; novelty judgment fragility. Situational safety benchmarks for multimodal LLMs.
- Genomic and specialized domain models expanding research tools (including OpenAI GPT-Rosalind-6 biology model). Hydrogen-1.0 scientific MoE. AlphaGenome 2 cell-specific genomics.
- Cost-aware abstention, agent phishing benchmarks, parameter learning in active inference.
- HoloBoxing: simple recipe for humanoid boxing with 7 minutes of single-GPU training.
- Google DeepMind PlanAssist: reduces UK planning officer assessment time by up to 58%; expanding to more councils.
- Role-induced sponsorship bias in decision models; disparity laundering in clinical multi-agent systems.
- Caution on alleged model leaks (e.g., Anthropic Mythos reports).
- Weight-space programming: frontier models reading and editing smaller model weights without gradients. Tree-Ising bit-level Ising edits for model repair.
- Voluntary Servitude: Weaponized safety warning mechanisms for controlling AI agents.

---

*Prefer updating an existing bullet with new results or status over creating near-duplicate entries.*
