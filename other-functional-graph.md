# functional-graph

## Intention
**Functional graph iteration, cycle detection, tree decomposition, and period analysis for x → f(x) mappings.**

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
A **functional graph** is a directed graph where every node has exactly one outgoing edge. Formally, for a function `f: V → V`, each node `x` has exactly one successor `f(x)`. These structures appear naturally in:

- **Iterated function systems** — repeatedly applying a function and studying orbits
- **Pseudo-random number generators** — each state maps to exactly one next state
- **Pollard's rho

## Who Would Use It
Add to your `Cargo.toml`:

```toml
[dependencies]
functional-graph = "0.1.0"
```

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (150 line README).

## Honest Assessment
Moderately documented (150 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/functional-graph](https://github.com/SuperInstance/functional-graph)*
