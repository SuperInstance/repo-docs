# lau-witten-reward

## Intention

lau-witten-reward

## How It Works

This crate applies **Witten deformation** and **Morse theory** to AI reward landscapes. It treats the reward function as a Morse function on the state space, then uses the full machinery of differential topology to analyze its structure:
- **Where are the reward basins?** → Critical points of index 0 (minima of the reward landscape)
- **How do basins connect?** → Instanton tunneling between critical points of adjacent index
- **Is the agent reward-hacking?** → Spurious tunneling detected via H¹ (first cohomology)
- **Is the reward landscape supersymmetric?** → Dirac operator D = d + δ, with D² = Δ
The core insight: **reward hacking is spurious tunneling between reward basins that shouldn't be connected.** The Witten complex captures this: H¹ measures the dimension of illegitimate pathways through the reward landscape.

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. lau-witten-reward

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (219 lines), mentions tests, includes examples.

- README length: 303 lines, 11808 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (303 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
