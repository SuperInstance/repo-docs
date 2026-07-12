# lau-state-machine

## Intention

Hierarchical state machine for agents and game entities — deterministic transitions, guards, actions.

## How It Works

`lau-state-machine` provides:
1. **A `StateMachine`** with hierarchical states — child states inherit transitions from parent states, enabling "any state → Flee" patterns without enumerating every source state.
2. **Priority-based conflict resolution** — when multiple transitions match, the highest-priority one wins.
3. **Named guard functions** — transitions can be conditional on `GuardEvaluator` predicates that inspect event data.
4. **A fluent builder** (`StateMachineBuilder`) for declaratively constructing machines.
5. **A pre-built `AgentStateMachine`** with 8 states (Idle, Wander, FollowPlayer, Flee, Interact, Work, Rest, Alert) and standard game-agent transitions.
6. **Full serialization** — the entire machine state (current state, history, tick count) round-trips through JSON.
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Hierarchical state machine for agents and game entities — deterministic transitions, guards, actions.

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (191 lines), mentions tests, includes examples.

- README length: 272 lines, 9106 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
