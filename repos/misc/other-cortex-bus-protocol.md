# cortex-bus-protocol

**Cluster:** fleet-agent-infra  
**Language:** Rust  
**Source:** [SuperInstance/cortex-bus-protocol](https://github.com/SuperInstance/cortex-bus-protocol)

## Intention

Rust exocortex crate: cortex-bus-protocol

## How It Works

[code]

## What It's For

Rust exocortex crate: cortex-bus-protocol

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (295 lines, 10567 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# cortex-bus-protocol

> **Command → Event → Query. CQRS for agent cognition.**

[![crates.io](https://img.shields.io/crates/v/cortex-bus-protocol.svg)](https://crates.io/crates/cortex-bus-protocol)
[![docs.rs](https://docs.rs/cortex-bus-protocol/badge.svg)](https://docs.rs/cortex-bus-protocol)
[![license](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

A Rust library implementing a CQRS event-sourced message bus for agent systems. Commands express intent, Events record facts, Queries read projections. Full event replay, projection rebuilding, and time-travel debugging for multi-agent architectures.

---

## Table of Contents

- [What is CQRS + Event Sourcing?](#what-is-cqrs--event-sourcing)
- [Why Does This Matter?](#why-does-this-matter)
- [Architecture](#architecture)
- [Quick Start](#quick-start)
- [API Reference](#api-reference)
- [Technical Background](#technical-background)
- [Installation](#installation)
- [Related Crates](#related-crates)
- [License](#license)

---

## What is CQRS + Event Sourcing?

**CQRS** (Command Query Responsibility Segregation) separates the write model (commands, events) from the read model (queries, projections). **Event Sourcing** stores every state change as an immutable event, enabling full replay and time-travel debugging.

```
┌──────────────────────────────────────────────────────────┐
│                     Write Side                           │
│                                                          │
│  Command ──► CommandHandler ──► Event ──► EventStore     │
│  (intent)    (validates)       (fact)    (append-only)   │
│                                                          │
├──────────────────────────────────────────────────────────┤
│                     Read Side                            │
│                                                          │
│  EventStore ──► Projection ──► Query ──► Result          │
│  (replay)      (read model)   (ask)     (answer)         │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

The key principles:

- **Commands** are imperative: "Do this thing" (may be rejected)
- **Events** are declarative: "This thing happened" (immutable facts)
- **Queries** ask questions of projections (derived read models)
- **Projections** are built from events (can be rebuilt at any time)

## Why Does This Matter?

**For agent debugging**: Every agent decision is recorded as an event. You can replay the full history, rebuild any past state, and answer "what went wrong?" with forensic precision.

**For multi-agent coordination**: Events are the shared truth between agents. Each agent maintains its own projections from the shared event stream — no race conditions, no distributed locks.

**For auditability**: In production agent systems, you need to know *why* an agent did something. Event sourcing gives you a complete audit trail: every command, every decision, every state change.

**For ev
```
