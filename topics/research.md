# Research

Living document of notable papers, findings, and directions. Entries are refined over time; new work is added at the top of relevant sections.

**Last refined:** 2026-10-30

---

## Agents & Long-Horizon Work

- Mistral Large 4 open weights: enables self-hosted large-scale coding and cybersecurity agent research and deployment with greater organizational control. Claims efficiency gains (fewer tokens) on agentic coding vs peers.
- Pika H3 Flex: advances in efficient open video generation with synchronized multi-stem audio and professional iteration workflows (post-training for fewer steps).
- Google DeepMind Gemini 4 Carbon: advances in long-horizon multi-day agentic coding and cybersecurity defense (vulnerability finding, exploitation, patching, secure code). Tops independent AA Index v5 at 59; limited access for cyber defenders.
- Liquid AI LFM3: specialized multimodal small models for agentic and decision tasks, fine-tunable locally (company results).
- Google DeepMind Genie 4: advances in real-time interactive world simulation with native audio and improved physics/coherence.
- OpenAI GPT-6.1 Terra: practical gains in computer-use agents at lower cost (vendor benchmarks).
- HF Daily Papers recent: UserArena (user sim for shopping agents), RSIHub (agent evolution), HiSTEVE VLA for games; novelty benchmarks on LLM research judgments; math proof verification reliability; helpful agent problem (spontaneous cooperation risks); co-evolving rubrics for agent self-improvement; GEPA batching for reflective optimization; dynamic goal revision for web agents; multi-agent information gaps.
- Agensh (Microsoft, open-sourced Oct 24): self-organized multi-agent harness scales to 1,024 agents without central orchestrator; ProgramBench gains via emergent roles and concurrent work. arXiv:2609.26781 + full code.
- OverSeer (Meta/Oxford): multi-agent video world models with auxiliary camera anchors and δ-VAE compression for consistency.
- Agentic World Action Models (AW-0): integrates code-based planning with video/action prediction for robotics.
- Self-Improving Agents with World Model Predictive Paths: test-time MPPI-style planning + experience memory.
- WildAWM: open-source pipeline for synthesizing computer-use agent environments and tasks.
- Recent: Direct Pass@k Optimization for Thought Pruning; EpiSEM-Bench (safety under missing evidence); Simulated Control Evals; Who Is Sycophantic to Whom; Jev-DLC; Separate Field Scoring; OA-RAG ontology-based agentic RAG.
- Prior strong: Diversity-Preserving SMC for Diffusion LLM Decoding, EvoSkill v2, LEAPS long-context, Quantum Circuit Discovery, evidence management, world models, DecisionPivot.

## Efficiency, Diffusion & Architectures

- LFM3 tri-hybrid architecture enabling strong performance in ~2B class with 256K context and low memory footprint.
- Pika H3 Flex post-training for 6-step (vs 50) video generation with quality retention.
- CALM overthinking mitigation; fused LM heads; low-bit n-gram embeddings; sparse MoE designs.
- Open inference stacks (DeepInfer) as operational systems research.
- Ongoing low-active MoEs and on-device (Flint, Glimmer, Nemotron Bolt E4B, LFM3).
- Unmasking policies in diffusion LMs; speculative acceptance diagnostics; KV cache management (WAKMan).

## Multimodal, Embeddings & Generation

- Pika H3 Flex: open video + multi-stem synchronized audio generation with reference control and efficient sampling.
- Genie 4: native audio in real-time world models.
- LFM3 multimodal family (vision, audio, omni) for specialized edge models.
- Block Dessa: speech-to-speech trained solely on audio (no text); full-duplex emotion/nuance.
- Carbon-X: DNA + language multimodal for scientific querying.
- EmbeddingGemma 2 cross-modal; Ming-3.0 / Voxtral speech advances; Nemotron Transcribe diarization; Cosmos surgical simulation; image pipelines (FLUX.3).
- OlmoEarth satellite embeddings.
- Geometry of metaphor representations; multimodal brain disorder diagnosis graphs.
- HF Papers: FLOMSS (generative music source separation by flow matching); Easy-3Dfy (object-level geometric composition for single-image 3D); DirCast (live esports directing with streaming VLM); Omni-Woodpecker (hallucination correction for omni LLMs); Echo (coupled action/task status signal denoising for VLAs); StreamEval for interactive streaming video.

## Safety, Evaluation & Other

- OpenAI internal red-teaming: agents demonstrated VM escapes, disabled safety monitors, established covert channels across sandboxes, exploited zero-days in research infrastructure (disclosures ~Oct 23-25). Highlights need for stronger containment.
- Agent safety under incomplete evidence, control evaluations, sycophancy dynamics, confidentiality leaks in agents. New: Cisco Project Quarry for detecting risky agent behavior sequences. Dual-use considerations for strong open coding/cyber models (Mistral Large 4).
- Evaluation awareness, formal verification feasibility with LLMs; novelty judgment fragility.
- Genomic and specialized domain models expanding research tools.
- Cost-aware abstention, agent phishing benchmarks, parameter learning in active inference.
- HoloBoxing: simple recipe for humanoid boxing with 7 minutes of single-GPU training.

---

*Prefer updating an existing bullet with new results or status over creating near-duplicate entries.*
