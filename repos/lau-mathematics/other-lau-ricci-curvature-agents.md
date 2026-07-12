# lau-ricci-curvature-agents

## Intention

lau-ricci-curvature-agents

## How It Works

This crate applies **discrete Ricci curvature** — a notion of curvature for graphs — to agent interaction networks. The key insight:
- **High curvature** = agents agree, fast consensus, robust information flow
- **Low/negative curvature** = agents disagree, information bottlenecks, slow convergence
- **Zero curvature** = random mixing, no structure
The crate computes two types of discrete Ricci curvature:
1. **Ollivier-Ricci curvature** — via optimal transport between neighborhood measures: `κ(x,y) = 1 - W₁(μₓ, μᵧ)/d(x,y)`
2. **Forman-Ricci curvature** — a simpler combinatorial formula: `F(u,v) = 4 - deg(u) - deg(v)`
It then uses curvature to detect bottlenecks, bound consensus times, verify Bonnet-Myers diameter bounds, and evolve fleet topology to improve convergence.
**96 tests** cover graph construction, both curvature types, concentration inequalities, Bonnet-Myers, curvature flow, and bottleneck detection.

## What It's For

lau-ricci-curvature-agents

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (245 lines), mentions tests, includes examples.

- README length: 336 lines, 12014 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (336 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
