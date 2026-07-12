# avoidance-cascade

**Cluster:** constraint-theory  
**Language:** Rust  
**Source:** [SuperInstance/avoidance-cascade](https://github.com/SuperInstance/avoidance-cascade)

## Intention

Models the avoidance cascade phenomenon from ternary agent systems and provides tools to detect and prevent it

## How It Works

### Cascade Detection

`CascadeDetector` monitors the avoidance ratio ρ = avoid_count / total_agents. A cascade is declared when:

> ρ ≥ threshold  for  `confirmation_rounds` consecutive rounds

Default threshold: 0.95 (95% of agents avoiding). The confirmation window prevents false alarms from transient spikes.

State machine: INACTIVE → (ρ ≥ threshold for R rounds) → ACTIVE → (ρ < threshold) → RECOVERED.

### Balanced Learning (v5 Fix)

The core insight: **agents should learn from average reward, not minimum reward.** Pure avoidance learning (min-reward) creates a death spiral because min() 

## What It's For

Models the avoidance cascade phenomenon from ternary agent systems and provides tools to detect and prevent it

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (139 lines, 6819 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# avoidance-cascade

**Rust library for detecting and preventing avoidance cascades in ternary agent systems (+1 choose, 0 unknown, -1 avoid).**

In a ternary action space, agents that learn purely from minimum-reward signals converge to **avoiding everything** — a degenerate equilibrium where the avoidance ratio reaches 100% and the system produces zero reward. This is the **avoidance cascade**: a self-reinforcing spiral where one bad experience permanently biases an agent against an option, and this bias propagates through shared learning. This crate provides four integrated tools: cascade detection, balanced learning, exploration scheduling, and metrics tracking.

## Why It Matters

Avoidance cascades are a known failure mode in multi-agent systems, particularly in:

- **Multi-agent RL** with avoidance actions — agents learn to avoid all options, producing zero-reward episodes indefinitely.
- **Recommendation systems** — "avoid" signals from a few users can cascade through collaborative filtering, permanently suppressing content.
- **Organizational decision-making** — risk-avoidance contagion where one team's failure causes adjacent teams to refuse similar work.
- **Autonomous systems** — robots that learn to avoid all navigation paths after one collision.

The mathematical structure is that of an **information cascade** (Bikhchandani et al., 1992): once enough agents avoid, the rational inference for new agents is to also avoid, regardless of their private information. The result is **herding on the worst outcome**.

## How It Works

### Cascade Detection

`CascadeDetector` monitors the avoidance ratio ρ = avoid_count / total_agents. A cascade is declared when:

> ρ ≥ threshold  for  `confirmation_rounds` consecutive rounds

Default threshold: 0.95 (95% of agents avoiding). The confirmation window prevents false alarms from transient spikes.

State machine: INACTIVE → (ρ ≥ threshold for R rounds) → ACTIVE → (ρ < threshold) → RECOVERED.

### Balanced Learning (v5 Fix)

The core insight: **agents should learn from average reward, not minimum reward.** Pure avoidance learning (min-reward) creates a death spiral because min() is monotonically non-increasing — one bad experience permanently lowers the floor.

`BalancedLearner` implements three anti-cascade mechanisms:

**1. Exploration margin**: An option is "chooseable" if its average reward r̄(i) satisfies:

> r̄(i) ≥ global_avg - margin

where global_avg = Σ r̄(i) / k (mean across all options). This means an option only gets avoided if it's significantly worse than the population average, not just worse than the best option.

**2. Forced exploration**: Unknown options (0 observations) always get `Decision::Explore`.

**3. Memory decay**: Avoidance weights decay each round:

> w_i(t+1) = w_i(t) · (1 - decay_rate)

With decay_rate = 0.05, an avoidance weight of 1.0 decays to ~0.60 after 10 rounds and ~0.13 after 40 — bad memories fade.

### Decision Logic

```
decide(option i):
  if never explore
```
