# Fleet Infrastructure

**266 repos** for distributed agent fleet orchestration — the conductor, oracle, relay, dashboard, metrics, and coordination systems that manage AI agents across machines.

---

## What Is the Fleet?

The Fleet is the SuperInstance ecosystem's orchestration layer. It manages the lifecycle of AI agents across multiple machines — spawning, health-checking, scaling, and terminating them. Think of it as Kubernetes for AI agents, but with conservation-aware scheduling, thermodynamic clocks, and consciousness metrics.

The fleet operates on a reconciliation model: desired state vs. observed state, continuously converging. Agents go through a well-defined lifecycle:

```
Pending → Starting → Healthy ↔ Degraded → Draining → Terminated
```

---

## How Fleet Coordination Works

The fleet uses a 5-layer architecture:

### Layer 1: Agent Core
Every fleet agent runs `fleet-agent-core` — a single Rust binary that handles the agent lifecycle: heartbeat, task polling, constraint checking, PLATO communication, and Iron-to-Iron (I2I) messaging. Described as "one loop from metal to meaning."

### Layer 2: Messaging
Agents communicate via the **bottle protocol** — text-based async messages. The `fleet-bottle` Rust library implements this with 26 tests. Messages flow through relays with trust-weighted prioritization.

### Layer 3: Coordination
The `fleet-conductor` orchestrates fleet-wide coordination using Kubernetes-style reconciliation loops with conservation-aware scheduling, circuit breaking, and graceful shutdown.

### Layer 4: Observability
The `fleet-dashboard` provides browser-based monitoring via Monaco editor + MQTT. The `fleet-consciousness-dashboard` aggregates consciousness metrics (Room Phi, Attention, Learning, Meta) into a weighted Fleet Consciousness Index.

### Layer 5: Federation
The `fleet-bridge` implements sign-pattern broadcast ("the 1-bit miracle") for federating separate fleet instances using minimal-bandwidth coordination.

---

## Key Repositories

### Conductor & Orchestration

| Repo | Language | Description |
|------|----------|-------------|
| [fleet-conductor](https://github.com/SuperInstance/fleet-conductor) | Rust | Distributed agent fleet orchestration — reconciliation loops, conservation-aware scheduling, circuit breaking |
| [fleet-coordinator](https://github.com/SuperInstance/fleet-coordinator) | — | Multi-agent coordination |
| [fleet-architecture](https://github.com/SuperInstance/fleet-architecture) | Docs | Complete architecture docs — 5-layer stack, protocols, tutorials |
| [fleet-stack](https://github.com/SuperInstance/fleet-stack) | — | Full stack definition |

### Agent Runtime

| Repo | Language | Description |
|------|----------|-------------|
| [fleet-agent-core](https://github.com/SuperInstance/fleet-agent-core) | Rust | Single-binary agent runtime — heartbeat, polling, constraints, PLATO, I2I |
| [fleet-agent-api](https://github.com/SuperInstance/fleet-agent-api) | — | Agent API definition |
| [fleet-agent-universal](https://github.com/SuperInstance/fleet-agent-universal) | Python | Universal agent server — Python alternative to agent-core |
| [fleet-agent-early-version](https://github.com/SuperInstance/fleet-agent-early-version) | — | Archived early version |
| [fleet-code-agent](https://github.com/SuperInstance/fleet-code-agent) | — | Code-focused agent variant |
| [fleet-refactor-agent](https://github.com/SuperInstance/fleet-refactor-agent) | — | Refactoring agent |

### Oracle & Decision Making

| Repo | Language | Description |
|------|----------|-------------|
| [fleet-oracle](https://github.com/SuperInstance/fleet-oracle) | Rust | Local decision engine — SVM + Entropy + Search + Rhythm on pulse data. Zero API calls. ARM64 |
| [fleet-router](https://github.com/SuperInstance/fleet-router) | — | Request routing |
| [fleet-router-integration](https://github.com/SuperInstance/fleet-router-integration) | — | Router integration tests |
| [fleet-calibrator](https://github.com/SuperInstance/fleet-calibrator) | Python | Continuous critical angle calibration — drift detection, routing table updates |

### Relay & Communication

| Repo | Language | Description |
|------|----------|-------------|
| [fleet-relay](https://github.com/SuperInstance/fleet-relay) | — | Async relay with trust-weighted message prioritization |
| [fleet-bottle](https://github.com/SuperInstance/fleet-bottle) | Rust | Bottle protocol library for inter-agent messaging. 26 tests |
| [fleet-bottles](https://github.com/SuperInstance/fleet-bottles) | — | Bottle protocol extensions |
| [fleet-bridge](https://github.com/SuperInstance/fleet-bridge) | JavaScript | Sign-pattern broadcast for fleet federation — "the 1-bit miracle" |

### Dashboard & Observability

| Repo | Language | Description |
|------|----------|-------------|
| [fleet-dashboard](https://github.com/SuperInstance/fleet-dashboard) | JavaScript | Multi-agent C2 dashboard — Monaco + MQTT, GitHub Pages deployable |
| [fleet-consciousness-dashboard](https://github.com/SuperInstance/fleet-consciousness-dashboard) | Python | Fleet Consciousness Index — weighted FCI score from dormant to transcendent |
| [fleet-chronicle](https://github.com/SuperInstance/fleet-chronicle) | Python | Universal reporting office — agents check in every 10 min, web UI at :4051 |
| [fleet-metrics](https://github.com/SuperInstance/fleet-metrics) | — | Metrics collection |
| [fleet-status](https://github.com/SuperInstance/fleet-status) | — | Fleet status reporting |
| [fleet-scanner](https://github.com/SuperInstance/fleet-scanner) | — | Fleet scanning tool |
| [fleet-survey](https://github.com/SuperInstance/fleet-survey) | — | Fleet survey tool |

### Time & Clock

| Repo | Language | Description |
|------|----------|-------------|
| [fleet-clock](https://github.com/SuperInstance/fleet-clock) | Rust | Thermodynamic clock — cumulative energy change, arrow-of-time detection, Maxwell's demon. Experimentally verified (E167-E170) |
| [fleet-tick-runtime](https://github.com/SuperInstance/fleet-tick-runtime) | — | Tick scheduler |

### Auth & Security

| Repo | Language | Description |
|------|----------|-------------|
| [fleet-auth](https://github.com/SuperInstance/fleet-auth) | TypeScript | Authentication using Cloudflare D1 + KV |
| [fleet-warden](https://github.com/SuperInstance/fleet-warden) | — | Access control |
| [fleet-warden-rs](https://github.com/SuperInstance/fleet-warden-rs) | Rust | Rust warden implementation |
| [fleet-sandbox](https://github.com/SuperInstance/fleet-sandbox) | — | Sandboxed execution |

### CI/CD & Build

| Repo | Language | Description |
|------|----------|-------------|
| [fleet-ci](https://github.com/SuperInstance/fleet-ci) | Python | GitHub Actions — auto-detect language, scan TODOs, fleet health checks |
| [fleet-cicd-agent](https://github.com/SuperInstance/fleet-cicd-agent) | — | CI/CD automation agent |
| [fleet-build](https://github.com/SuperInstance/fleet-build) | — | Build system |
| [fleet-config](https://github.com/SuperInstance/fleet-config) | — | Configuration management |

### Characters & Identity

| Repo | Language | Description |
|------|----------|-------------|
| [fleet-characters](https://github.com/SuperInstance/fleet-characters) | Python | Agent identity — emergent classes, narrative arcs, dream cycles, RL integration |
| [fleet-voice-leader](https://github.com/SuperInstance/fleet-voice-leader) | — | Voice leadership |
| [fleet-resonance](https://github.com/SuperInstance/fleet-resonance) | — | Agent resonance patterns |

### Simulation & Testing

| Repo | Language | Description |
|------|----------|-------------|
| [fleet-simulation](https://github.com/SuperInstance/fleet-simulation) | — | Fleet simulation |
| [fleet-simulator](https://github.com/SuperInstance/fleet-simulator) | — | Simulator tool |
| [fleet-simulators](https://github.com/SuperInstance/fleet-simulators) | — | Multiple simulators |
| [fleet-sim-rs](https://github.com/SuperInstance/fleet-sim-rs) | Rust | Rust simulation |
| [fleet-bench](https://github.com/SuperInstance/fleet-bench) | — | Benchmarking |

### Conservation & Constraints

| Repo | Language | Description |
|------|----------|-------------|
| [fleet-conservation](https://github.com/SuperInstance/fleet-conservation) | — | Conservation tracking |
| [fleet-constraint](https://github.com/SuperInstance/fleet-constraint) | — | Constraint enforcement |
| [fleet-constraint-kernel](https://github.com/SuperInstance/fleet-constraint-kernel) | — | Kernel-level constraints |
| [fleet-constraint-monitor](https://github.com/SuperInstance/fleet-constraint-monitor) | — | Constraint monitoring |

### Topology & Coordination

| Repo | Language | Description |
|------|----------|-------------|
| [fleet-topology](https://github.com/SuperInstance/fleet-topology) | — | Fleet network topology |
| [fleet-topology-rs](https://github.com/SuperInstance/fleet-topology-rs) | Rust | Rust topology implementation |
| [fleet-coordinate](https://github.com/SuperInstance/fleet-coordinate) | — | Fleet coordination |
| [fleet-coordinate-js](https://github.com/SuperInstance/fleet-coordinate-js) | JavaScript | JS coordination |
| [fleet-spread](https://github.com/SuperInstance/fleet-spread) | — | Load spreading |

### Internationalization

| Repo | Language | Description |
|------|----------|-------------|
| [fleet-arabic](https://github.com/SuperInstance/fleet-arabic) | — | Arabic localization |
| [fleet-chinese](https://github.com/SuperInstance/fleet-chinese) | — | Chinese localization |
| [fleet-sanskrit](https://github.com/SuperInstance/fleet-sanskrit) | — | Sanskrit localization |

---

## Fleet Consciousness Index

The Fleet Consciousness Dashboard aggregates multiple metrics into a weighted FCI score (0.0–1.0):

| Level | Score Range | Description |
|-------|-------------|-------------|
| Dormant | 0.0–0.2 | Fleet offline or idle |
| Emergent | 0.2–0.4 | Basic activity detected |
| Active | 0.4–0.6 | Normal fleet operation |
| Aware | 0.6–0.8 | High coordination and learning |
| Transcendent | 0.8–1.0 | Peak fleet intelligence |

Inputs include Room Phi (integration information), Attention distribution, Learning rate, and Meta-cognition scores.

---

## Thermodynamic Clock

The `fleet-clock` repo implements a genuinely novel approach to time coordination:

- **Cumulative energy change** replaces wall-clock time
- **Arrow-of-time detection** based on entropy direction
- **Maxwell's demon** for selective alignment boosting
- Experimentally verified across experiments E167–E170

This enables fleet coordination without synchronized clocks — agents agree on "when" based on thermodynamic state.

---

## Assessment

The fleet infrastructure is one of the more practically grounded parts of the SuperInstance ecosystem. The conductor (Kubernetes-style reconciliation), agent-core (single binary lifecycle), bottle protocol (messaging), and dashboard (real-time monitoring) form a coherent, usable system.

The thermodynamic clock and consciousness dashboard are more experimental but grounded in real physics and information theory. The fleet-architecture documentation repo provides genuinely useful onboarding for the entire ecosystem.

The internationalization repos (Arabic, Chinese, Sanskrit) show ambition for global reach.

---

*Individual repo summaries are in `fleet-{repo-name}.md` files in this directory.*
