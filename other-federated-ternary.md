# federated-ternary

## Intention
**Federated learning over ternary weight spaces** — multiple nodes train {-1, 0, +1} weight vectors locally, then merge via element-wise majority vote. The merge operation is commutative, associative, and idempotent (CRDT properties), making it Byzantine-tolerant without coordination.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
Standard federated learning (FedAvg) averages continuous-valued weights — but averaging is vulnerable to Byzantine participants (a single malicious node can shift the average arbitrarily). Ternary federated learning replaces averaging with **majority voting**, which is far more robust:

- **Byzantine tolerance**: With n nodes and f < n/2 Byzantine, the majority still converges to the correct weigh

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (136 line README).

## Honest Assessment
Moderately documented (136 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/federated-ternary](https://github.com/SuperInstance/federated-ternary)*
