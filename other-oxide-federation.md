# oxide-federation

## Intention
Multi-node GPU cluster federation with ternary health states. Gossip health, work stealing, quorum decisions, graceful degradation.

## How It Works
Cross-cluster GPU federation with gossip health, work stealing, quorum decisions, and graceful degradation. Single GPU clusters are easy. Multiple clusters across data centers, availability zones, or cloud providers are not. When you federate GPU resources, you face four problems simultaneously: how do nodes learn each other's state (gossip), how do you move work from overloaded to underloaded nodes (stealing), how do you make decisions without a single coordinator (quorum), and what happens when a node disappears (degradation). The ternary health model solves the coordination problem cleanly. Each node is Healthy (+1, accepts work), Recovering (0, warming up), or Offline (-1, dead). Gossip propagates these states. Quorum requires a majority of healthy nodes among active voters. Work steal

## What It's For
Multi-node GPU cluster federation with ternary health states. Gossip health, work stealing, quorum decisions, graceful degradation.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 7,056 characters, 156 lines
- Code examples: 5 blocks
- Installation instructions: no
- Testing mentioned: no
- License mentioned: no
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (5 code blocks)
- Solid README with good coverage

**Concerns:**
- No clear installation instructions
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
