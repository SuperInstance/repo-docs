# lever-runner

## Intention

Post-inference command executor. A token-lean AI operator that runs pre-approved shell commands by intent, not by tool schemas.

## How It Works

```
You type:  "check disk usage on the server"
│
┌──────────────▼──────────────┐
│ Gate 1: Rust fastloop (50µs)│──► template match? ──► df -h
└──────────────┬──────────────┘     miss ↓
┌──────────────▼──────────────┐
│ Gate 2: Python cache (200µs)│──► embedding hit? ──► df -h
└──────────────┬──────────────┘     miss ↓
┌──────────────▼──────────────┐
│ Gate 3: LLM (500ms)         │──► "show disk usage"
│   sees ONLY the phrase      │    (8 tokens, not 2000)
└──────────────┬──────────────┘
│
┌──────────────▼──────────────┐

## What It's For

Post-inference command executor. A token-lean AI operator that runs pre-approved shell commands by intent, not by tool schemas.

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Python

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (329 lines), mentions tests, includes examples, has benchmarks.

- README length: 432 lines, 14771 characters
- Documented sections: 30 seconds, The problem with AI shell tools, The insight: you don't need an LLM at runtime, Real numbers, Quick start

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (432 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**

> ⚠️ **Ecosystem dependency:** This repo makes 3+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
