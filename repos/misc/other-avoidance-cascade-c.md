# avoidance-cascade-c

**Cluster:** constraint-theory  
**Language:** C  
**Source:** [SuperInstance/avoidance-cascade-c](https://github.com/SuperInstance/avoidance-cascade-c)

## Intention

C implementation of avoidance cascade detection and prevention for ternary agents

## How It Works

### Cascade Detection

The detector counts avoid actions across the population each round, computes the avoid ratio $\gamma = |\text{avoid}| / n$, and compares against a threshold $\theta$ (typically 0.95). A cascade is declared when $\gamma > \theta$ for **3 consecutive rounds** — this hysteresis prevents false positives from transient spikes.

[code]

**Complexity**: $O(n)$ per round for counting, $O(1)$ for comparison. Space: $O(1)$ for state (stores only ratios in history buffer).

### Balanced Learner

The balanced learner tracks per-option reward using an **Exponential Moving Average (EM

## What It's For

C implementation of avoidance cascade detection and prevention for ternary agents

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

C — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (173 lines, 8038 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# avoidance-cascade-c — Detection and Prevention of Avoidance Cascades in Ternary Agent Systems

**avoidance-cascade-c** is a C library that detects and prevents **avoidance cascades** — the catastrophic failure mode where agents in a ternary decision system (each choosing between Avoid −1, Unknown 0, or Choose +1) progressively converge toward avoidance until the entire population refuses all actions. The library provides a cascade detector with configurable thresholds, a balanced learner with exponential moving average reward tracking, and an exploration scheduler with exponential decay to inject forced exploration.

## Why It Matters

In multi-agent reinforcement learning, avoidance cascades are a well-documented collapse mode: when agents share information and observe peers avoiding actions, avoidance propagates contagiously through the population. This is analogous to **bank runs** in financial systems — rational individual decisions aggregate into collectively irrational outcomes. In production fleets, an avoidance cascade means every agent stops processing requests, creating a total system blackout. This library provides the detection and correction primitives needed to guarantee that the avoid ratio $\gamma_{\text{avoid}}$ never exceeds a safety threshold for more than a bounded number of consecutive rounds, with $O(n)$ detection cost per round.

## How It Works

### Cascade Detection

The detector counts avoid actions across the population each round, computes the avoid ratio $\gamma = |\text{avoid}| / n$, and compares against a threshold $\theta$ (typically 0.95). A cascade is declared when $\gamma > \theta$ for **3 consecutive rounds** — this hysteresis prevents false positives from transient spikes.

```
round r: γ_r = count(actions == AVOID) / n
if γ_r > θ:
    cascade_rounds++
    if cascade_rounds ≥ 3: cascading = true
else:
    cascade_rounds = 0
    cascading = false
```

**Complexity**: $O(n)$ per round for counting, $O(1)$ for comparison. Space: $O(1)$ for state (stores only ratios in history buffer).

### Balanced Learner

The balanced learner tracks per-option reward using an **Exponential Moving Average (EMA)** with decay factor $\alpha$:

$$\hat{r}_i^{(t)} = \alpha \cdot \hat{r}_i^{(t-1)} + (1 - \alpha) \cdot r_i^{(t)}$$

The decision logic is ternary:
1. **Forced exploration**: Every `explore_interval` steps, return UNKNOWN (explore) regardless of learned rewards.
2. **Avoid**: If the best-known option has $\hat{r}_{\text{best}} < \text{margin}$, the learner returns AVOID — all options are worse than the safety margin.
3. **Choose**: If the best-known option exceeds the margin, return CHOOSE (exploit).

This prevents the degenerate case where a learner with no good options keeps choosing the least-bad option. The margin parameter implements a **reservation threshold** — familiar from the secretary problem and bandit literature.

### Exploration Scheduler

The scheduler controls exploration rate $\epsilon$ with exponential 
```
