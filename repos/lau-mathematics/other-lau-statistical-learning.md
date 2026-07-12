# lau-statistical-learning

## Intention

Statistical learning theory — the mathematical foundations of machine learning.

## How It Works

`lau-statistical-learning` provides **10 modules** covering the mathematical backbone of ML theory:
1. **`bias_variance`** — Decompose prediction error into bias² + variance + noise. Generate theoretical U-shaped tradeoff curves.
2. **`vc_dimension`** — VC dimension descriptors for common hypothesis classes (intervals, linear classifiers, rectangles), growth function bounds (Sauer-Shelah), generalization bounds.
3. **`pac_learning`** — PAC sample complexity for both realizable and agnostic settings, generalization gap verification.
4. **`rademacher`** — Empirical Rademacher complexity via Monte Carlo, Massart's lemma, Rademacher generalization bounds.
5. **`cross_validation`** — K-fold and leave-one-out cross-validation with configurable shuffling and seeds.
6. **`regularization`** — L1 (Lasso), L2 (Ridge), and Elastic Net penalty computation with coefficient paths.
7. **`kernel`** — RBF (Gaussian), polynomial, and linear kernels with a `Kernel` trait, Gram matrix computation.
8. **`svm`** — Hard-margin and soft-margin SVMs with SMO-style optimization, kernelized decision boundaries.
9. **`learning_curves`** — Inverse-root learning curve models, sample complexity estimation, training/test error curves.
10. **`agent_learning`** — Multi-armed bandit (ε-greedy + UCB1), regret analysis, confidence intervals, simulation.
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Statistical learning theory — the mathematical foundations of machine learning.

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (354 lines), mentions tests, includes examples.

- README length: 491 lines, 15778 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (491 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
