# plato-nervous

## Intention
Room-specific model distillation for PLATO rooms — the nervous system signal chain (Sensor → Deadband → Nano → LoRA → Fleet → Cloud)

## How It Works
> The full PLATO signal chain: Sensor → Deadband → Nano → LoRA → Fleet → Cloud plato-nervous implements PLATO's tiered intelligence pipeline. Sensor readings come in at the bottom and each layer resolves what it can, escalating only the hard problems upward. Most readings are handled by simple algorithmic filters (deadband). A few need the nano-model. Rarely, a room-specific LoRA adapter. Almost never, the cloud LLM. This is the nervous system: fast local reflexes, slower centralized reasoning.

## What It's For
Part of the PLATO ecosystem. Room-specific model distillation for PLATO rooms — the nervous system signal chain (Sensor → Deadband → Nano → LoRA → Fleet → Cloud)

## Who Would Use It
PLATO ecosystem developers and SuperInstance fleet operators.

## Language / Stack
Rust

## Status Assessment
🟢 Substantial — comprehensive documentation with architecture, examples, API refs

## Honest Assessment
Core component with thorough documentation, architecture diagrams, code examples, and test coverage. This is production-track work, not a stub.

## README Substance Level
- **Size:** 3305 bytes
- **Substance:** substantial
- **Has code examples:** True
- **Mentions testing:** True
- **Sections:** What This Does, The Key Idea, Install, Quick Start, API Reference, Testing, License
