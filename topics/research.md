# Research

Living document of notable papers, findings, and directions. Entries are refined over time; new work is added at the top of relevant sections.

**Last refined:** 2026-10-15

---

## Agents & Long-Horizon Work

- **QwenGyre** — Elastic RL framework for extreme-long (“xLong”) agent tasks spanning hours and ~1M tokens.
- **ColGrep-Agent-2B** — Local search agent that reduces context tax for coding assistants by moving repository exploration to a small model.
- Continued focus on agent memory systems, goal persistence, and recovery from intermediate failures.

## Efficiency & On-Device

- Robotics inference distillation (RealtimeWAM-style and related): large speedups (~25×) with minimal success-rate degradation for real-time control loops.
- Low-active-parameter MoEs and hybrid architectures for edge / laptop deployment remain a major theme (LFM2.5, MiniCPM-V 4.7).
- **VKORE-46M-NPU**: Full training loop (backpropagation) demonstrated on an inference-first NPU.

## Safety, Security & Evaluation

- Anthropic Frontier Red Team: research indicating small models may soon be capable of self-replication on commercial IoT devices.
- **SWE-DeceptionBench** and related work on deceptive behaviors of LLMs across the software development lifecycle.
- Prompt-injection and agent safety benchmarks continue to matter for frontier model releases (e.g., Argon reported strong results).
- Practical evaluation blueprint for domain-specific speech recognition (NVIDIA ATC study).

## Model Internals & Editing

- Speculative decoding improvements (e.g., DLoop-style multi-round verification; DSpark heads for MiniCPM-V 4.7).
- Fact / knowledge editing approaches such as EngramEdit (editing conditional memory / n-gram tables).
- Decision models (Lumma-Fev-27B and related): explicit choice + probability outputs instead of free generation.

## Multimodal & Embeddings

- Cross-modal embedding models (EmbeddingGemma 2 and similar) enabling shared spaces for text, image, audio, and video.
- Multimodal decision and vision-language models (decision heads, MoE VLMs like MiniCPM-V 4.7).
- **HiRO-ACEv2**: Extreme weather simulation at 3 km resolution at fraction of prior cost.

---

*Prefer updating an existing bullet with new results or status over creating near-duplicate entries.*