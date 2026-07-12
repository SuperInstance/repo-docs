# shell-mesh

## Intention
Shell Mesh — distributed command mesh for fleet-wide agent coordination

## How It Works
Dynamic mesh networking for heterogeneous device fleets — ESP32 to cloud, self-organizing. A Rust library for building mesh topologies that detect their own structure, route messages, and adapt as nodes join and leave. Designed for the SuperInstance fleet: devices from microcontrollers to GPUs collaborating in real-time. - Self-organizing topology — automatically detects star, full-mesh, hierarchical, or custom layouts - Typed device nodes — ESP32, Jetson, Desktop, Server, Cloud — each with capabilities and status - Structured messaging — Discovery, ResourceOffer, TaskRequest, TaskResult, Heartbeat - Serde-serializable — every type derives Serialize/Deserialize for network transport

## What It's For
Shell Mesh — distributed command mesh for fleet-wide agent coordination

## Who Would Use It
Rust developers building AI agent fleets

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 3,175 characters, 96 lines
- Code examples: 3 blocks
- Installation instructions: yes
- Testing mentioned: yes
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: no

## Honest Assessment

**Strengths:**
- Code examples present (3 code blocks)
- Installation/usage instructions provided
- Testing mentioned

**Concerns:**
- None immediately apparent from README alone

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
