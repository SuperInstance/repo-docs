# room-dds-bridge

## Intention
Auto-configure DDS domains from ternary-mud room topology

## How It Works
Auto-configure DDS (Data Distribution Service) domains from ternary-mud room topology — map spatial relationships to publish/subscribe topics, QoS policies, and domain bridges. Given a topology of rooms connected by passages, room-dds-bridge computes DDS domain assignments, generates topic definitions, derives QoS policies from ternary {-1, 0, +1} passage state, and serializes the complete configuration to JSON. DDS is the middleware standard for real-time distributed systems (aerospace, autonomous vehicles, industrial IoT). Configuring DDS by hand — domains, topics, QoS, pub/sub assignments — is tedious and error-prone for systems with many nodes. This crate automates that mapping from a higher-level spatial topology description, ensuring:

## What It's For
Auto-configure DDS domains from ternary-mud room topology

## Who Would Use It
Rust developers

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 5,735 characters, 121 lines
- Code examples: 1 blocks
- Installation instructions: yes
- Testing mentioned: no
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Installation/usage instructions provided
- Solid README with good coverage

**Concerns:**
- None immediately apparent from README alone

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
