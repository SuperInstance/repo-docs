# dissertation-engine

## Intention
**Dissertation Engine** is a Rust crate providing the computational backbone for the dissertation *"Intelligence is Models for the Negative Space"*, reproducing all key figures and results from five empirically discovered laws of ternary agent systems.

## How It Works
**Law 1 — Negative Space Discovers:**
A reinforcement-learning agent on a 1-D strip with N = 20 positions, 60% marked dangerous. The agent receives *only* negative feedback: reward = −1 for danger, 0 otherwise. Using a simple value update:

```
V(s) ← V(s) + α(r − V(s))     // α = 0.1
```

With ε-greedy exploration (ε = 0.05), the agent learns to avoid danger zones. After 200 episodes of 500 steps each, avoidance rate exceeds 0.55 — demonstrating that purely negative feedback suffices to discove

## What It's For
This crate is the reproducible computational artifact for a set of five mathematical laws governing ternary agent systems with action space {-1, 0, +1} (Avoid, Unknown, Choose). Each law was discovered through simulation and is verified here with deterministic, seeded experiments. The laws span behavioral psychology (avoidance dominates approach by 294:1), ecology (competitive species coexist with

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (76 line README).

## Honest Assessment
Has documentation (76 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/dissertation-engine](https://github.com/SuperInstance/dissertation-engine)*
