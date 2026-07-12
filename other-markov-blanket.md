# markov-blanket

## Intention

> Where does an agent end and the world begin? The Markov blanket knows.

## How It Works

In probability theory, the **Markov blanket** of a node in a Bayesian network is the minimal set of nodes that shields it from the rest of the network. Once you know the values of the blanket nodes, the target node becomes conditionally independent of everything else.
Formally, for a node X in a Bayesian network, its Markov blanket consists of:
- **Parents**: nodes that directly influence X
- **Children**: nodes that X directly influences
- **Co-parents**: other parents of X's children (they explain away competing causes)
This concept is central to the **Free Energy Principle** (Karl Friston, 2006), where the blanket separates an agent's internal states from external states. Everything an agent can know about the world must come through its Markov blanket — sensory states (what it observes) and active states (what it does).
```
┌─────────────────────────────────────────────┐
│                External States               │
│         (the environment, hidden)            │
├─────────────────────────────────────────────┤
│         ┌─────────┐   ┌─────────┐           │
│         │ Sensory │   │ Active  │           │
│         │ States  │   │ States  │ ← Blanket │
│         └────┬────┘   └────┬────┘           │

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. > Where does an agent end and the world begin? The Markov blanket knows.

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (185 lines), mentions tests, includes examples, has benchmarks.

- README length: 251 lines, 10019 characters
- Documented sections: Table of Contents, What is a Markov Blanket?, Why Does This Matter?, Architecture, Quick Start

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
