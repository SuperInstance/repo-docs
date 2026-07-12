# oxide-health-monitor

## Intention
GPU health monitoring with ternary status. Auto-failover redistributes work from failed nodes. CRDT sync across monitoring agents.

## How It Works
GPU health monitoring with ternary status signals and CRDT-based distributed sync. GPU hardware fails. Memory errors, thermal throttling, PCIe link degradation, power supply flakiness. When a GPU starts failing, you need to detect it fast, route work away from it, and let the rest of the cluster absorb the load. But health isn't binary — a GPU can be fully operational (Healthy, +1), degraded but functional (Degraded, 0), or dead (Failed, -1). Treating everything as "up or down" means you either overreact to transient issues or underreact to slow degradation. The CRDT merge strategy means multiple health monitors can observe the same fleet independently and merge their observations without coordination. Failed overrides everything (fail-fast). Degraded propagates but doesn't override Failed

## What It's For
GPU health monitoring with ternary status. Auto-failover redistributes work from failed nodes. CRDT sync across monitoring agents.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 5,936 characters, 146 lines
- Code examples: 4 blocks
- Installation instructions: no
- Testing mentioned: no
- License mentioned: no
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (4 code blocks)
- Solid README with good coverage

**Concerns:**
- No clear installation instructions
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
