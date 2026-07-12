# analog-spectral

**Cluster:** constraint-theory  
**Language:** Rust  
**Source:** [SuperInstance/analog-spectral](https://github.com/SuperInstance/analog-spectral)

## Intention

Analog eigenvalue computation. Dials settle under gravity. Deadband = spectral gap. The thermostat IS the algorithm. Pure Rust, zero deps.

## How It Works

[code]

## What It's For

Analog eigenvalue computation. Dials settle under gravity. Deadband = spectral gap. The thermostat IS the algorithm. Pure Rust, zero deps.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (257 lines, 9796 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# analog-spectral

**Eigenvalue estimation as mechanical settling — physical dials converge under gravity, friction creates deadbands equal to spectral gaps, and the thermostat IS the algorithm.**

> *What if eigenvalue computation isn't a numerical procedure but a physical process? Dials settling under gravity toward eigenvalue setpoints, with friction creating the deadbands that are spectral gaps. The Jacobi algorithm is just a bunch of dials finding equilibrium.*

---

## The Problem

Eigenvalue computation is fundamental to spectral graph theory, conservation analysis, and the entire SuperInstance ecosystem. But numerical algorithms abstract away the physics. What if you could *see* the computation happening — dials turning, springs pulling, friction resisting — and the settled positions *were* the eigenvalues?

This matters because the physical analogy reveals structure that pure numerics hides: the deadband (friction/gravity) is exactly the spectral gap between eigenvalues, the settling time predicts convergence rate, and the precision is bounded by thermal noise in exactly the way floating-point is bounded by mantissa bits.

## The Key Insight

**A damped harmonic oscillator converging to a setpoint IS eigenvalue iteration.**

Consider a single analog dial:
- **Position** = current eigenvalue estimate
- **Setpoint** = true eigenvalue
- **Gravity** = restoring force strength (convergence rate)
- **Friction** = damping coefficient
- **Deadband** = friction/gravity = spectral gap

The equation of motion is:
```
m·ẍ = −gravity·(x − setpoint) − friction·ẋ
```

Within the deadband (|x − setpoint| < friction/gravity), friction dominates and the dial stops. This deadband IS the spectral gap — the region where the eigenvalue estimate is "close enough" that numerical noise dominates further convergence.

For N coupled dials, the coupling matrix determines inter-dial forces. When the bank settles, the dial positions approximate eigenvectors and the Rayleigh quotient gives the eigenvalue. **This IS the Jacobi eigenvalue algorithm, but phrased as physical dynamics.**

## Architecture

```
 ┌─────────────────────────────────────────────────┐
 │                    DialBank                      │
 │  N coupled dials + coupling matrix              │
 │                                                 │
 │  ┌─────────┐ ┌─────────┐       ┌─────────┐    │
 │  │ Dial 0  │ │ Dial 1  │ ···   │ Dial N  │    │
 │  │ pos=λ₀  │ │ pos=λ₁  │       │ pos=λₙ  │    │
 │  └────┬────┘ └────┬────┘       └────┬────┘    │
 │       │            │                 │          │
 │       └────────────┼─────────────────┘          │
 │                    │                            │
 │            coupling matrix A                    │
 │         (inter-dial forces)                     │
 └────────────┬────────────────────────────────────┘
              │
              ▼
 ┌─────────────────────────┐    ┌──────────────────────┐
 │    SpectralGapAnalysis  │    │  PrecisionAnalysis   │
```
