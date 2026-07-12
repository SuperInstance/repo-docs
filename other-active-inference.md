# active-inference

**Cluster:** ai-cognitive  
**Language:** Rust  
**Source:** [SuperInstance/active-inference](https://github.com/SuperInstance/active-inference)

## Intention

See README.

## How It Works

[code]

## What It's For

See README.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (265 lines, 10798 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# active-inference

> **Act to reduce uncertainty. The Free Energy Principle in motion.**

[![crates.io](https://img.shields.io/crates/v/active-inference.svg)](https://crates.io/crates/active-inference)
[![docs.rs](https://docs.rs/active-inference/badge.svg)](https://docs.rs/active-inference)
[![license](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

A Rust library implementing active inference — the framework that unifies perception and action under a single imperative: minimize expected free energy. Agents don't just perceive the world; they act on it to reduce future uncertainty. Implements policy enumeration, expected free energy evaluation, precision-weighted action selection, and Bayesian state estimation.

---

## Table of Contents

- [What is Active Inference?](#what-is-active-inference)
- [Why Does This Matter?](#why-does-this-matter)
- [Architecture](#architecture)
- [Quick Start](#quick-start)
- [API Reference](#api-reference)
- [Mathematical Background](#mathematical-background)
- [Installation](#installation)
- [Related Crates](#related-crates)
- [License](#license)

---

## What is Active Inference?

Active inference (Friston et al., 2015) extends the Free Energy Principle from perception to action. An agent doesn't just update beliefs to match observations — it acts on the world to make observations match its beliefs. The result: perception and action are two sides of the same minimization process.

The **active inference loop**:

```
   ┌──────────────────────────────────────────────┐
   │                                              │
   │  1. Observe    →  sensory state arrives      │
   │  2. Infer      →  update beliefs (perception)│
   │  3. Predict    →  compute G(π) for policies  │
   │  4. Select     →  pick π with lowest G       │
   │  5. Execute    →  first action of chosen π   │
   │       │                                      │
   │       └──────→ new observation → repeat ──→  │
   │                                              │
   └──────────────────────────────────────────────┘
```

The key equation is **expected free energy** G(π) for a policy π:

```
G(π) = risk(π) + ambiguity(π)
     = KL[q(s|π) || p(s)] + E[H[p(o|s)]]
```

- **Risk**: divergence from preferred states (pragmatic value)
- **Ambiguity**: expected uncertainty in observations (epistemic value)

Agents prefer policies that reach preferred states AND reduce uncertainty. This naturally produces exploration behavior without any explicit exploration bonus.

## Why Does This Matter?

**Unified framework**: No separate reward function, exploration bonus, or value network. A single quantity (expected free energy) produces goal-directed behavior, exploration, and risk avoidance.

**Biological plausibility**: Active inference describes how real nervous systems work — dopamine encodes precision, not reward. Place cells minimize expected free energy. Saccades are epistemic actions.

**Balanced exploration-exploitation**: The epistemic (informati
```
