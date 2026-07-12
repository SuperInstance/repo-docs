# persistent-social

## Intention
Persistent homology for social network analysis — pure Go, goroutine-safe, 10K+ scale

## How It Works
Topological data analysis for social networks in Go — Vietoris-Rips filtration, persistent homology, Wasserstein distances, and mobility/stratification metrics. Computes the topological fingerprint of social networks. People are vertices, relationships are edges with strength weights. Builds a Vietoris-Rips filtration, computes H⁰ and H¹ persistence, and extracts interpretable metrics: mobility score (how transient relationships are), stratification index (how many permanent structures exist), and community count. - Social graph construction — people with attributes, weighted edges - Vietoris-Rips filtration — growing epsilon threshold on edge weights - Persistent homology — H⁰ (communities) and H¹ (structural holes/bridges) - Wasserstein distance — compare two social networks topologicall

## What It's For
Persistent homology for social network analysis — pure Go, goroutine-safe, 10K+ scale

## Who Would Use It
Go developers in computational topology / data analysis

## Language / Stack
Go

## Status Assessment
**Developing** — Moderate documentation with some structure and examples.

- README size: 2,368 characters, 66 lines
- Code examples: 3 blocks
- Installation instructions: yes
- Testing mentioned: yes
- License mentioned: yes
- API documentation: no
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Deep theoretical grounding (5 advanced math concepts referenced)
- Code examples present (3 code blocks)
- Installation/usage instructions provided
- Testing mentioned

**Concerns:**
- Heavy abstraction may limit practical adoption
- Unclear if theoretical rigor translates to working software

**Overall:** Early but potentially interesting — read the source to verify.
