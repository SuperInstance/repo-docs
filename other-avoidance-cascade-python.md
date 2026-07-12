# avoidance-cascade-python

**Cluster:** constraint-theory  
**Language:** Python  
**Source:** [SuperInstance/avoidance-cascade-python](https://github.com/SuperInstance/avoidance-cascade-python)

## Intention

Models and fixes the avoidance cascade phenomenon from ternary agent systems

## How It Works

### SIR-Style Contagion Model

The `SpreadModel` implements a discrete-time epidemic model on ternary agents:

> State transitions per step:
> - AVOIDING → (1 - recovery_rate) → stays AVOIDING
> - AVOIDING → recovery_rate → NEUTRAL
> - AVOIDING contacts NEUTRAL neighbor j with probability contagion_rate → j becomes AVOIDING

Each avoider contacts `contact_degree` random neighbors per step. The force of infection on a single neutral agent is:

> λ = β · c · (I/N)

where β = contagion_rate, c = contact_degree, I = # avoiders, N = population.

The basic reproduction number:

> R₀ = β · c · D = β 

## What It's For

Models and fixes the avoidance cascade phenomenon from ternary agent systems

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (164 lines, 7630 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# avoidance-cascade-python

**Python toolkit for detecting, modeling, and intervening in avoidance cascades in ternary agent populations.**

In a ternary action space (+1 = engaged, 0 = neutral, -1 = avoiding), agents that learn purely from negative signals can enter a **cascade failure**: one bad experience causes avoidance, which biases neighbors toward avoidance, which cascades until the entire population is avoiding everything. This crate provides contagion models (SIR-style spread), cascade detection (rolling-window threshold), tipping point analysis (velocity + acceleration), intervention simulation (vaccinate/quarantine/boost), and balanced learning with forced exploration.

## Why It Matters

Avoidance cascades are a documented failure mode in multi-agent reinforcement learning, social network dynamics, and organizational behavior. The mathematics parallel **epidemic spreading** (SIR/SEIR models from epidemiology):

- An avoiding agent (infected) can convert neutral agents (susceptible) through contact
- The **basic reproduction number R₀** determines whether avoidance spreads or dies out
- **Herd immunity** threshold: if enough agents are "engaged" (vaccinated), the cascade cannot sustain itself

This matters for:

- **Multi-agent RL** — agents that all learn to avoid produce zero reward, a degenerate equilibrium
- **Social media** — pile-on dynamics where one negative review triggers universal rejection
- **Organizational decision-making** — risk aversion cascading through a hierarchy
- **Algorithmic fairness** — automated systems that learn to avoid certain demographics

## How It Works

### SIR-Style Contagion Model

The `SpreadModel` implements a discrete-time epidemic model on ternary agents:

> State transitions per step:
> - AVOIDING → (1 - recovery_rate) → stays AVOIDING
> - AVOIDING → recovery_rate → NEUTRAL
> - AVOIDING contacts NEUTRAL neighbor j with probability contagion_rate → j becomes AVOIDING

Each avoider contacts `contact_degree` random neighbors per step. The force of infection on a single neutral agent is:

> λ = β · c · (I/N)

where β = contagion_rate, c = contact_degree, I = # avoiders, N = population.

The basic reproduction number:

> R₀ = β · c · D = β · c / γ

where γ = recovery_rate and D = 1/γ = average infection duration.

R₀ > 1 → epidemic (cascade spreads). R₀ < 1 → die-out.

### Cascade Detection

`CascadeDetector` uses a sliding window of W recent observations. At each step:

> ρ(t) = (# avoiding in window) / (total in window)

Alert fires when ρ(t) ≥ threshold (default 0.5). The detector tracks:
- `avoidance_ratio` — current ρ
- `engaged_ratio` — current fraction of +1 agents
- `neutral_ratio` — 1 - ρ - engaged_ratio

### Tipping Point Detection

Three methods operate on the avoidance ratio time series:

**Threshold**: fires when ρ crosses threshold τ.

**Velocity**: fires when |ρ(t) - ρ(t-1)| ≥ v_threshold (first derivative).

**Acceleration**: fires when |Δ²ρ(t)| ≥ a_threshold (second derivative). Thi
```
