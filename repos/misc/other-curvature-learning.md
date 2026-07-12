# curvature-learning

**Cluster:** ai-cognitive  
**Language:** Rust  
**Source:** [SuperInstance/curvature-learning](https://github.com/SuperInstance/curvature-learning)

## Intention

Agents learning on curved manifolds — Riemannian gradient descent and natural gradient

## How It Works

[code]

**Flow:** The `manifold` defines the space. `metric` measures distances. `christoffel` computes how the basis twists. `geodesic` finds straight paths. `gradient` uses all of it for optimization. `fisher` brings information geometry to parameter distributions.

## What It's For

Agents learning on curved manifolds — Riemannian gradient descent and natural gradient

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (368 lines, 15141 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# curvature-learning

**Agents learning on curved manifolds — Riemannian gradient descent and natural gradient.**

An agent doesn't learn in a vacuum. It learns in a landscape — and that landscape has curvature. When your parameters are probabilities on a simplex, rotations in SO(3), or points on a hyperbolic surface, flat Euclidean gradient descent is climbing hills in shoes that don't fit. The geometry of the space fights you. Steps that look equal in parameter space are wildly unequal in reality.

`curvature-learning` provides the geometric primitives for learning *with* the curvature instead of against it. Riemannian gradient descent follows the natural geodesics of parameter space. Natural gradient uses the Fisher information matrix to measure how much a parameter change actually changes the distribution. The result: fewer steps, more stable convergence, and parameterization-invariant learning.

This is the math that makes agents learn like they have a sense of direction, not just a sense of slope.

## The Metaphor: Curved Learning Landscapes

Imagine an agent navigating a mountain range. Standard gradient descent tells it "walk downhill" — but the map is flat. The agent doesn't know about ravines, ridges, or the fact that a step east might cover more ground than a step north because the terrain slopes differently.

Now give the agent a *topographic map*. Not just elevation, but the full metric tensor: how distances warp and stretch across the landscape. Suddenly the agent knows:

- **Where steps are expensive** (steep curvature → short geodesic steps)
- **Where steps are cheap** (flat regions → long geodesic steps)  
- **How to walk straight** (follow geodesics, not coordinate lines)
- **How to carry its compass** (parallel transport preserves direction)

This is what Riemannian geometry gives a learning agent. The manifold is the landscape. The metric tensor is the topographic map. Geodesics are the shortest paths. And the Christoffel symbols? They're the terrain's way of saying *"your compass is drifting — here's how to correct it."*

In the SuperInstance ecosystem:
- **`categorical-agents`** reason about discrete choices — their parameter spaces are simplices, where the Fisher metric reigns
- **`tropical-neural`** reshapes neural computation with tropical algebra — the geometry is different but the curvature principles are the same
- **`symplectic-opt`** optimizes over phase spaces where the symplectic structure constrains learning trajectories
- **`curvature-learning`** provides the *shared language of curvature* that all of them speak

## Architecture

```
                    ┌──────────────────────────────────┐
                    │        curvature-learning         │
                    └──────────────────────────────────┘
                                   │
          ┌────────────────────────┼────────────────────────────┐
          │                        │                            │
    ┌─────▼─────┐          ┌──────▼──────┐   
```
