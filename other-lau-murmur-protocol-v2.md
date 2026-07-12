# lau-murmur-protocol-v2

## Intention

Gossip-based information spreading with epidemic models. How rumors (and truths) spread through agent networks.

## How It Works

```rust
use lau_murmur_protocol_v2::*;
// Create a network
let topo = NetworkTopology::small_world(20, 2, 0.3);
let mut net = GossipNetwork::new(topo);
// Inject a rumor
let m = net.inject("agent-0", "the sky is falling", vec!["urgent".into()]);
// Simulate
net.run(10);
println!("Coverage: {:.1}%", net.coverage(&m.id) * 100.0);
```

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Gossip-based information spreading with epidemic models. How rumors (and truths) spread through agent networks.

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: LIGHT**

Short README (38 lines), includes examples.

- README length: 50 lines, 1571 characters
- Documented sections: Components, Usage, Theorems Verified

## Honest Assessment

Part of the sprawling Lau/PLATO ecosystem. The README covers basics but the project is one of many math/computation crates in this organization. The breadth of repos in SuperInstance (hundreds) raises questions about depth vs. breadth — many appear to be auto-generated or lightly documented. **This crate likely works as a component but standalone value is limited without the broader ecosystem.**
