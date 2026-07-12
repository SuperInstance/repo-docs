# creative-engine-rust

**Cluster:** content-creative  
**Language:** Rust  
**Source:** [SuperInstance/creative-engine-rust](https://github.com/SuperInstance/creative-engine-rust)

## Intention

Rust implementation of the Creative Dynamics Engine — dynamical systems for modeling creative processes.

## How It Works

It Fits

- **[creative-engine-c](https://github.com/SuperInstance/creative-engine-c)** — The C original; this is the Rust port
- **[constraint-hamiltonian](https://github.com/SuperInstance/constraint-hamiltonian)** — Add constraint surfaces to creative trajectories
- **[flux-algebra-rs](https://github.com/SuperInstance/flux-algebra-rs)** — Map Lorenz coordinates to pitch/class space via harmonic rings
- **[counterpoint-engine-rs](https://github.com/SuperInstance/counterpoint-engine-rs)** — Evaluate creative output against counterpoint rules

## What It's For

Rust implementation of the Creative Dynamics Engine — dynamical systems for modeling creative processes.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (102 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# creative-engine-rust

Rust port of [creative-engine-c](https://github.com/SuperInstance/creative-engine-c) — Lorenz attractors, regime detection, Kuramoto synchronization, quality metrics, coupling, and adaptive thermostats for generative creative processes.

## What This Gives You

- **`CreativeSystem`** — Single Lorenz system with RK4 stepping, output tracking, and quality measurement
- **Regime detection** — Classify as fixed-point, periodic, or chaotic based on output statistics
- **Quality metrics** — Novelty (variety), coherence (self-similarity), combined quality score
- **Kuramoto coupling** — Synchronize multiple creative systems into coherent ensembles
- **Adaptive thermostat** — Tune exploration/exploitation based on output quality
- **Builder API** — Configure σ, ε, and other parameters fluently
- **Zero dependencies** — Pure Rust, `std` only

## Quick Start

```rust
use creative_engine::CreativeSystem;

let mut sys = CreativeSystem::new(28.0);  // ρ = 28 → chaotic regime
sys.run(1000, 200);  // 1000 steps, discard 200 transient

// Detect regime
let regime = sys.detect_regime();  // Regime::Chaotic

// Quality metrics
let q = sys.quality();
println!("novelty={} coherence={} quality={}", q.novelty, q.coherence, q.quality);

// Builder-style configuration
let mut sys = CreativeSystem::new(28.0)
    .with_sigma(12.0)
    .with_epsilon(0.3);
```

### Coupled systems (Kuramoto)

```rust
use creative_engine::CoupledSystem;

let mut coupled = CoupledSystem::new(3, 28.0)  // 3 coupled Lorenz systems
    .with_coupling(0.1);                        // coupling strength
coupled.run(500, 100);
println!("sync order: {}", coupled.order_parameter());  // → 1.0 = fully synced
```

## API Reference

### `CreativeSystem`

| Method | Description |
|--------|-------------|
| `new(rho)` | Create system with given ρ parameter |
| `run(steps, transient)` | Integrate and collect outputs |
| `detect_regime()` | Classify as `Regime::Fixed`, `Periodic`, or `Chaotic` |
| `quality()` | `QualityMetrics { novelty, coherence, quality }` |
| `diversity()` | Standard deviation of outputs |
| `with_sigma(s)` / `with_epsilon(e)` | Builder configuration |

### `CoupledSystem`

| Method | Description |
|--------|-------------|
| `new(n, rho)` | N coupled systems |
| `with_coupling(k)` | Set coupling strength |
| `order_parameter()` | Kuramoto order parameter (0.0–1.0) |

## How It Fits

- **[creative-engine-c](https://github.com/SuperInstance/creative-engine-c)** — The C original; this is the Rust port
- **[constraint-hamiltonian](https://github.com/SuperInstance/constraint-hamiltonian)** — Add constraint surfaces to creative trajectories
- **[flux-algebra-rs](https://github.com/SuperInstance/flux-algebra-rs)** — Map Lorenz coordinates to pitch/class space via harmonic rings
- **[counterpoint-engine-rs](https://github.com/SuperInstance/counterpoint-engine-rs)** — Evaluate creative output against counterpoint rules

## Testing

35 tests covering Lorenz integration, regi
```
