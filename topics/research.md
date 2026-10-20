# Research

Living document of notable papers, findings, and directions. Entries are refined over time; new work is added at the top of relevant sections.

**Last refined:** 2026-10-20

---

## Agents & Long-Horizon Work

- **Quantum Circuit Discovery** (Anthropic/Harvard/QuEra, Oct 19): LLM + evolutionary search discovers efficient reversible quantum circuits and new algorithms (e.g., improved modular inversion).
- **LongHarness / Evidence Management**: Gains on long-context agent reasoning via stateful evidence handling rather than raw chat history.
- **AnyGoal / World Models**: Generalization of world models beyond expert rollouts for planning.
- Tool-output retrieval accuracy costs; imaginative agents (Sokoban-style foresight); computer-use environment synthesis; ProteinGeoBench (agents strong at lookup, weaker on geometry).
- Prior: FDE-Gym, MLExpert, Terminal-RSI, AgentCIScope, EvoSafeHarness.

## Efficiency, Diffusion & Architectures

- Fused LM heads and training optimizations enabling longer sequences / lower VRAM.
- Text-to-image without language pretraining (Halcyon family).
- Flexible representation learning for unified multimodal models.
- Continued low-active-parameter MoEs and on-device designs.

## Multimodal, Embeddings & Generation

- EmbeddingGemma 2 cross-modal embeddings (text/image/audio/video).
- Ming-3.0 audio models advancing open speech/audio understanding and generation.
- Open image generation pipelines (FLUX 3 Klein, Qwen-Image).

## Safety, Evaluation & Other

- GRPO refinements for safety alignment; verifier feedback in formal proving.
- Frontend agentic RL (WebCoder); evaluation awareness and agent safety harnesses.

---

*Prefer updating an existing bullet with new results or status over creating near-duplicate entries.*
