# coalition-game

**Cluster:** rust-misc  
**Language:** Rust  
**Source:** [SuperInstance/coalition-game](https://github.com/SuperInstance/coalition-game)

## Intention

See README.

## How It Works

[code]

## What It's For

See README.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (338 lines, 12695 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# coalition-game

**Cooperative game theory in Rust: Shapley value, core, nucleolus, and stable coalition analysis.**

Every day, autonomous agents face a fundamental question: *who should I work with, and how do we split the gains?* Cooperative game theory provides the mathematical framework to answer this — from allocating costs in shared infrastructure to dividing rewards in multi-agent AI systems. `coalition-game` brings these tools to Rust with zero external dependencies beyond `serde`.

## Why this crate exists

You're building a multi-agent system where agents form alliances. One agent has data, another has compute, a third has domain expertise. Together they're worth more than the sum of their parts. How do you:

- **Fairly divide** the joint payoff? → Shapley value
- **Verify** that no subgroup would defect? → Core analysis
- **Find** the unique fair division that minimizes complaints? → Nucleolus
- **Check** if a coalition structure is stable? → Stability analysis

This crate implements the four pillars of cooperative game theory as composable, serializable Rust types. No C dependencies, no BLAS, no LaTeX — just clean, tested math.

## The metaphor: coalition games as cooperative intelligence

```
    Agent ○──── has data
    Agent ○──── has compute     ───→  Coalition ◉──── worth more together
    Agent ○──── has domain knowledge     than apart
```

Think of agents forming alliances. A single agent might be worth nothing alone, but the right coalition can solve problems none could tackle individually. Cooperative game theory is the mathematics of *cooperative intelligence* — it tells us which alliances form, how they share rewards, and whether those arrangements are stable.

The Shapley value is the unique fair division that satisfies four intuitive axioms. The core tells us whether an allocation is stable against defection. The nucleolus finds the allocation that minimizes the maximum complaint. Together, they form a complete toolkit for reasoning about cooperation.

## Architecture

```
┌──────────────────────────────────────────────────────────┐
│                    coalition-game                         │
│                                                          │
│  ┌────────────┐    ┌──────────────┐    ┌──────────────┐  │
│  │ coalition  │───▶│   value      │───▶│   shapley    │  │
│  │            │    │              │    │              │  │
│  │ Coalition  │    │ ValueFunction│    │ ShapleyValue │  │
│  │ bitmask    │    │ super/sub    │    │ exact/sample │  │
│  │ lattice    │    │ convex check │    │ axioms check │  │
│  └────────────┘    └──────┬───────┘    └──────────────┘  │
│                           │                               │
│                    ┌──────▼───────┐                       │
│                    │    core      │                       │
│                    │              │                       │
│                    │ Core         │                       │
│                    │ Bondareva-   │       
```
