# openconstruct-jetson

## Summary
GPU edge node on NVIDIA Jetson.

## Intention
OpenConstruct is the agent onboarding framework for the SuperInstance ecosystem — any agent, any hardware, any language.

## How It Works
C ABI as universal onboarding layer. Language-specific SDKs wrap the ABI. Agents call onboard() to register, then exchange messages via A2A protocol.

## What It's For
- Agent onboarding for the fleet (12+ language SDKs)
- Embedded and edge device integration
- Hardware-accelerated edge nodes

## Who Would Use It
- AI agent developers in any language
- Embedded/mobile developers
- Enterprise teams

## Language/Stack
- **Primary language:** C++
- **Ecosystem:** C ABI core with 12+ language bindings

## Status Assessment
**Early stage or stub.**

## Honest Assessment
GPU edge node on Jetson is practical for robotics/marine. Local inference reduces latency.
