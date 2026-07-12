# nash-finder

## Intention

Nash equilibrium computation for agent strategic interactions

## How It Works

### Zero External Dependencies (except serde)
Game theory is foundational mathematics. It shouldn't pull in a dependency tree
the size of a web framework. `serde` is the sole exception — serialization is
essential for persistence and interop.
### f64 Throughout
Game theory payoffs are inherently continuous. We use `f64` throughout for
numerical stability and simplicity. No generic numeric types.
### 2-Player Focus for Exact Solutions
Support enumeration is the primary exact algorithm, and it's specific to 2-player
games. For N-player games, the solver falls back to fictitious play and best-response
dynamics. This mirrors the state of the art: exact NE computation is tractable for
2 players, PPAD-complete for 3+.
### Verification as a First-Class Concern
Every equilibrium found by support enumeration is independently verified against
the best-response conditions. This catches numerical errors from Gaussian elimination

## What It's For

Nash equilibrium computation for agent strategic interactions

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (355 lines), mentions tests, includes examples.

- README length: 481 lines, 14510 characters
- Documented sections: Why This Crate Exists, The Metaphor: Agents as Game Theorists, Quick Start, Module Reference, Defining Games

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (481 lines) with tests, examples, and benchmarks referenced. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
