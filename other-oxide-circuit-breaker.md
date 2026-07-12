# oxide-circuit-breaker

## Intention
Circuit breaker pattern for GPU kernels. Track failure rates, trip on threshold, auto-failover to fallback. CRDT sync across fleet.

## How It Works
oxide-circuit-breaker A production-grade circuit breaker for GPU kernels, built in Rust. Protect your inference fleet from cascading failures with ternary-state semantics, automatic fallback routing, and CRDT-based fleet-wide synchronization. The Story: Why GPUs Need Circuit Breakers

## What It's For
Circuit breaker pattern for GPU kernels. Track failure rates, trip on threshold, auto-failover to fallback. CRDT sync across fleet.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 7,954 characters, 152 lines
- Code examples: 4 blocks
- Installation instructions: yes
- Testing mentioned: yes
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (4 code blocks)
- Installation/usage instructions provided
- Testing mentioned
- Solid README with good coverage

**Concerns:**
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
