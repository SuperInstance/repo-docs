# markov-chain

## Intention

A Markov chain library for modeling discrete-state stochastic processes where the next state depends only on the current state (the Markov property) — providing transition matrix construction, stationary distribution computation, and chain simulation.

## How It Works

**Transition matrix**: An N×N stochastic matrix P where `P[i][j]` = probability of transitioning from state i to state j. Each row sums to 1 (it's a probability distribution).
```
P = | 0.9  0.1  0.0 |    State 0: mostly stays, 10% → State 1
| 0.3  0.4  0.3 |    State 1: volatile, spreads across all
| 0.0  0.2  0.8 |    State 2: mostly stays, 20% → State 1
```
**n-step transitions**: P^n gives the probability of transitioning from i to j in exactly n steps. As n → ∞, P^n converges to a matrix where every row equals the stationary distribution π (if the chain is ergodic — irreducible and aperiodic).
**Stationary distribution**: The eigenvector of P^T corresponding to eigenvalue 1:
```
π · P = π     (left eigenvector)
Σ π_i = 1     (normalization)
```
This is the long-run proportion of time spent in each state. Computed via:
- **Power iteration**: π_{n+1} = π_n · P until convergence. O(N²) per iteration.
- **Direct eigendecomposition**: For small N, solve the linear system (P^T - I)π = 0 with constraint Σπ = 1.

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. A Markov chain library for modeling discrete-state stochastic processes where the next state depends only on the current state (the Markov property) — providing transition matrix construction, station

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (71 lines), includes examples.

- README length: 95 lines, 4395 characters
- Documented sections: Why It Matters, How It Works, Quick Start, API, Architecture Notes

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**

> ⚠️ **Ecosystem dependency:** This repo makes 3+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
