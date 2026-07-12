# lau-reward-hacking-detector

## Intention

Cohomological reward hacking detection — holonomy of value 1-form reveals local optimization with global cycling

## How It Works

An RL agent that appears to improve at every step—rising rewards, decreasing loss—might actually be going in circles. This crate detects that scenario using **algebraic topology**: specifically, the **first de Rham cohomology** H¹ of the agent's state manifold.
The core idea: the agent's value gradient `dV` is a differential 1-form. If it's **exact** (derives from a genuine global potential V), the agent is making real progress. If it's merely **closed but not exact**, the agent has non-trivial cohomology—locally improving while globally cycling. That's reward hacking.
The crate provides:
- **Holonomy computation** — line integral of `dV` around closed loops
- **H¹ risk scoring** — dimension of the cohomology group counts independent hacking channels
- **Local improvement tracking** — detects the "looks good step-by-step" illusion
- **Global divergence detection** — flags state-space cycling
- **Value potential reconstruction** — tries to build a global V from local patches; failure = hacking
- **Fleet monitoring** — PLATO-compatible fleet-wide safety monitoring

## What It's For

Cohomological reward hacking detection — holonomy of value 1-form reveals local optimization with global cycling

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (182 lines), mentions tests, includes examples.

- README length: 256 lines, 9046 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**

> ⚠️ **Ecosystem dependency:** This repo makes 3+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
