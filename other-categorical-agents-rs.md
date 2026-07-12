# categorical-agents-rs

**Cluster:** fleet-agent-infra  
**Language:** Rust  
**Source:** [SuperInstance/categorical-agents-rs](https://github.com/SuperInstance/categorical-agents-rs)

## Intention

See README.

## How It Works

Category-theoretic abstractions for composing agents.

## What It's For

See README.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (430 lines, 13977 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# categorical-agents-rs

Category-theoretic abstractions for composing agents.

Agents are morphisms. Agent pipelines are functors. Agent context is a comonad. Agent effects are a monad. Adjunctions bridge the gap between what an agent *is* and what an agent *does*.

This is not abstraction for its own sake. Category theory gives us laws — left identity, right identity, associativity, triangle identities — that compose correctly by construction. When you chain 50 agents in a pipeline, you want proofs, not prayers.

Part of the **sunset-ecosystem**: categorical composition provides the algebraic backbone for agent orchestration. `conservation-law` uses adjunctions to enforce resource invariants, and `si-fleet-api` dispatches composed agent programs across the fleet.

## The Math

### Categories, Objects, Morphisms

A **category** $\mathcal{C}$ consists of:
- A collection of **objects** $\text{Ob}(\mathcal{C})$
- For each pair $(A, B)$, a set of **morphisms** $\text{Hom}(A, B)$
- Composition $\circ: \text{Hom}(B, C) \times \text{Hom}(A, B) \to \text{Hom}(A, C)$
- Identity morphisms $\text{id}_A \in \text{Hom}(A, A)$

satisfying associativity and identity laws.

For agents: objects are agent types, morphisms are transformations between agent states.

### Functors

A **functor** $F: \mathcal{C} \to \mathcal{D}$ maps objects to objects and morphisms to morphisms, preserving composition and identity:

$$F(g \circ f) = F(g) \circ F(f)$$
$$F(\text{id}_A) = \text{id}_{F(A)}$$

`fmap` is functor application on morphisms.

### Monads

A **monad** on a category $\mathcal{C}$ is an endofunctor $T: \mathcal{C} \to \mathcal{C}$ equipped with:
- **return** ($\eta$): $A \to T(A)$
- **bind** ($\gg=$): $T(A) \to (A \to T(B)) \to T(B)$

satisfying three laws:
1. **Left identity**: $\text{return}(a) \gg= f \equiv f(a)$
2. **Right identity**: $m \gg= \text{return} \equiv m$
3. **Associativity**: $(m \gg= f) \gg= g \equiv m \gg= (\lambda x. f(x) \gg= g)$

### Comonads

A **comonad** is the dual: $W: \mathcal{C} \to \mathcal{C}$ with:
- **extract**: $W(A) \to A$
- **duplicate**: $W(A) \to W(W(A))$
- **extend**: $W(A) \to (W(A) \to B) \to W(B)$

Comonads model agents in context — an agent that can see its neighborhood, its history, its environment.

### Adjunctions

An **adjunction** $F \dashv G$ between functors $F: \mathcal{C} \to \mathcal{D}$ and $G: \mathcal{D} \to \mathcal{C}$ provides a natural isomorphism:

$$\text{Hom}_{\mathcal{D}}(F(A), B) \cong \text{Hom}_{\mathcal{C}}(A, G(B))$$

with unit $\eta: \text{Id} \to GF$ and counit $\varepsilon: FG \to \text{Id}$ satisfying the triangle identities.

### Distributional Functor

The `DistributionalFunctor` maps agent categories to performance distributions. Drift from a category is measured via the 1-Wasserstein distance between an agent's performance vector and the category's reference distribution.

## Installation

```toml
[dependencies]
categorical-agents-rs = { git = "https://github.com/SuperInstance/categorical-
```
