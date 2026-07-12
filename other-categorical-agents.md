# categorical-agents

**Cluster:** fleet-agent-infra  
**Language:** Rust  
**Source:** [SuperInstance/categorical-agents](https://github.com/SuperInstance/categorical-agents)

## Intention

Category theory for agents — capabilities as objects, protocols as morphisms, symmetric monoidal categories, functors

## How It Works

You have agents. One searches, one summarizes, one acts. How do you compose them? Not with ad-hoc glue code — with *algebra*.

[code]

## What It's For

Category theory for agents — capabilities as objects, protocols as morphisms, symmetric monoidal categories, functors

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (366 lines, 12584 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# categorical-agents

Composition of agents follows the same laws as composition of functions. You can reason about your fleet the same way you reason about your code.

## The Problem

You have agents. One searches, one summarizes, one acts. How do you compose them? Not with ad-hoc glue code — with *algebra*.

```rust
use categorical_agents::*;
```

---

## 1. Capabilities as Objects

Every agent has a capability — what it *does*. Capabilities are objects in a category.

```rust
use categorical_agents::Capability;

let search    = Capability::new("search").with_arity(1);
let summarize = Capability::new("summarize").with_arity(1);
let act       = Capability::new("act").with_arity(1);

println!("search:    {} (arity {})", search, search.arity);
println!("summarize: {} (arity {})", summarize, summarize.arity);
println!("act:       {} (arity {})", act, act.arity);

// The tensor product: "both at the same time"
let search_and_summarize = search.tensor(&summarize);
println!("{} ⊗ {} = {} (arity {})",
    search, summarize, search_and_summarize, search_and_summarize.arity);
// search ⊗ summarize = search⊗summarize (arity 2)
// This is parallel composition: both capabilities running simultaneously

// The unit: "do nothing"
let unit = Capability::unit();
println!("Unit: {} (arity {})", unit, unit.arity);
// I is the identity for tensor: A ⊗ I = A

// The dual: "the input side of a capability"
let input = Capability::new("input");
let dual = input.dual();
println!("Dual of {}: {}", input, dual);
// input → input* (the anti-capability, the type of data it consumes)

// Internal hom: "how to transform A into B"
let transform = search.internal_hom(&act);
println!("search ⊸ act = {}", transform);
// search*⊗act = "the capability of turning search results into actions"
```

**The tensor product IS parallel execution.** The dual IS the input type. The internal hom IS the transformation.

---

## 2. Protocols as Morphisms

A protocol connects one capability to another. It's a morphism in the category.

```rust
use categorical_agents::{Capability, Protocol};

let raw      = Capability::new("raw");
let encoded  = Capability::new("encoded");
let sent     = Capability::new("sent");
let received = Capability::new("received");

// Protocols: morphisms between capabilities
let encode = Protocol::new("encode", raw, encoded).with_cost(0.5);
let send   = Protocol::new("send", encoded, sent).with_cost(1.0);
let recv   = Protocol::new("receive", sent, received).with_cost(0.3);

println!("encode: {} → {} (cost: {})", encode.source, encode.target, encode.cost);
println!("send:   {} → {} (cost: {})", send.source, send.target, send.cost);

// Compose: g ∘ f means "do f, then do g"
let send_encoded = encode.compose(&send).unwrap();
println!("{} ∘ {} = {} → {} (cost: {})",
    send.name, encode.name, send_encoded.source, send_encoded.target, send_encoded.cost);
// send ∘ encode = raw → sent (cost: 1.5)
// f.target MUST equal g.source — type safety from the math

// Identity: "do
```
