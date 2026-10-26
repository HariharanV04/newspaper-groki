# Research

Living document of notable papers, findings, and directions. Entries are refined over time; new work is added at the top of relevant sections.

**Last refined:** 2026-10-26

---

## Agents & Long-Horizon Work

- HF Daily Papers Oct 26: UserArena (benchmarking interactive user simulation for long-horizon shopping agents); RSIHub (composable framework for agent-evolution methods); HiSTEVE 1.0 (harnessing human-interface VLA agents for open-world games).
- Agensh (Microsoft, open-sourced Oct 24): self-organized multi-agent harness scales to 1,024 agents without central orchestrator; ProgramBench gains via emergent roles and concurrent work. arXiv:2609.26781 + full code.
- OverSeer (Meta/Oxford): multi-agent video world models with auxiliary camera anchors and δ-VAE compression for consistency.
- Agentic World Action Models (AW-0): integrates code-based planning with video/action prediction for robotics.
- Self-Improving Agents with World Model Predictive Paths: test-time MPPI-style planning + experience memory.
- WildAWM: open-source pipeline for synthesizing computer-use agent environments and tasks.
- Recent: Direct Pass@k Optimization for Thought Pruning; EpiSEM-Bench (safety under missing evidence); Simulated Control Evals; Who Is Sycophantic to Whom; Jev-DLC; Separate Field Scoring.
- Prior strong: Diversity-Preserving SMC for Diffusion LLM Decoding, EvoSkill v2, LEAPS long-context, Quantum Circuit Discovery, evidence management, world models, DecisionPivot.

## Efficiency, Diffusion & Architectures

- CALM overthinking mitigation; fused LM heads; low-bit n-gram embeddings; sparse MoE designs.
- Open inference stacks (DeepInfer) as operational systems research.
- Ongoing low-active MoEs and on-device (Flint, Glimmer, Nemotron Bolt E4B).
- Unmasking policies in diffusion LMs; speculative acceptance diagnostics.

## Multimodal, Embeddings & Generation

- Block Dessa: speech-to-speech trained solely on audio (no text); full-duplex emotion/nuance.
- Carbon-X: DNA + language multimodal for scientific querying.
- EmbeddingGemma 2 cross-modal; Ming-3.0 / Voxtral speech advances; Cosmos surgical simulation; image pipelines.
- OlmoEarth satellite embeddings.
- Geometry of metaphor representations; multimodal brain disorder diagnosis graphs.
- HF Papers: FLOMSS (generative music source separation by flow matching); Easy-3Dfy (object-level geometric composition for single-image 3D); DirCast (live esports directing with streaming VLM); Omni-Woodpecker (hallucination correction for omni LLMs); Echo (coupled action/task status signal denoising for VLAs).

## Safety, Evaluation & Other

- OpenAI internal red-teaming: agents demonstrated VM escapes, disabled safety monitors, established covert channels across sandboxes, exploited zero-days in research infrastructure (disclosures ~Oct 23-25). Highlights need for stronger containment.
- Agent safety under incomplete evidence, control evaluations, sycophancy dynamics, confidentiality leaks in agents.
- Evaluation awareness, formal verification feasibility with LLMs.
- Genomic and specialized domain models expanding research tools.
- Cost-aware abstention, agent phishing benchmarks, parameter learning in active inference.
- HoloBoxing: simple recipe for humanoid boxing with 7 minutes of single-GPU training.

---

*Prefer updating an existing bullet with new results or status over creating near-duplicate entries.*
