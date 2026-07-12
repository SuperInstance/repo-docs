# boltzmann-agent

**Cluster:** fleet-agent-infra  
**Language:** Rust  
**Source:** [SuperInstance/boltzmann-agent](https://github.com/SuperInstance/boltzmann-agent)

## Intention

Boltzmann distribution applied to agent action selection and multi-agent systems

## How It Works

[code]

## What It's For

Boltzmann distribution applied to agent action selection and multi-agent systems

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (626 lines, 26764 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# boltzmann-agent

**Boltzmann distribution applied to agent action selection and multi-agent systems.**

A zero-dependency (except `serde`) Rust crate that brings the mathematical framework of statistical mechanics to computational agents. Temperature-controlled exploration/exploitation, simulated annealing optimization, detailed balance verification, multi-agent ensembles, and Friston's free energy principle—all in clean, well-documented Rust.

```
[dependencies]
boltzmann-agent = "0.1"
```

---

## Table of Contents

- [Theory](#theory)
- [Architecture](#architecture)
- [Quick Start](#quick-start)
- [Examples](#examples)
  - [Basic Boltzmann Distribution](#example-1-basic-boltzmann-distribution-computation)
  - [Action Selection with Temperature Annealing](#example-2-action-selection-with-temperature-annealing)
  - [Simulated Annealing Optimization](#example-3-simulated-annealing-optimization)
  - [Multi-Agent Ensemble Equilibrium](#example-4-multi-agent-ensemble-equilibrium)
- [Module Reference](#module-reference)
- [Design Decisions](#design-decisions)
- [Performance](#performance)
- [Comparison with Alternatives](#comparison-with-alternatives)
- [Glossary](#glossary)
- [References](#references)
- [License](#license)

---

## Theory

### The Boltzmann Distribution

The fundamental insight connecting statistical mechanics to agent systems is the **Boltzmann distribution** (also called the Gibbs distribution). For a system with discrete states {s₁, s₂, ..., sₙ}, each with energy E(sᵢ), the probability of observing the system in state sᵢ at temperature T is:

```
P(sᵢ) = exp(-E(sᵢ) / kT) / Z
```

where:

- **β = 1/(kT)** is the **inverse temperature** (higher β → more concentrated on low-energy states)
- **k** is Boltzmann's constant (set to 1 in natural units)
- **Z = Σᵢ exp(-E(sᵢ) / kT)** is the **partition function**, the normalization constant

This is the same distribution as the **softmax** function used in machine learning, but with physical interpretation: energies are costs, temperature controls exploration, and the partition function ensures valid probabilities.

### The Partition Function

The **partition function** Z is the single most important quantity in equilibrium statistical mechanics:

```
Z = Σᵢ exp(-βE(sᵢ))
```

From Z, every thermodynamic quantity can be derived:

| Quantity | Formula |
|----------|---------|
| Mean energy | ⟨E⟩ = -∂(ln Z)/∂β |
| Entropy | S = k·ln Z + ⟨E⟩/T = k(1 + ln Z - β⟨E⟩) |
| Free energy | F = -kT·ln Z |
| Specific heat | Cᵥ = ∂⟨E⟩/∂T = β²·Var(E)/k |

### Free Energy

**Helmholtz free energy** at constant temperature and volume:

```
F = ⟨E⟩ - TS = -kT·ln Z
```

This is the quantity that systems at equilibrium minimize. For agents, F captures the tradeoff between being in low-energy (accurate) states and maintaining high entropy (exploration):

- **Low F** → agent is both accurate *and* uncertain (exploring efficiently)
- **F = ⟨E⟩** when S = 0 (agent is certain but possibly wrong)
- **F → -kT·ln(N)
```
