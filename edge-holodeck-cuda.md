# holodeck-cuda

## Summary
GPU-resident holodeck (16K rooms).

## Intention
Holodeck is a MUD-style simulation environment for fleet modeling — rooms, agents, gauges, and scoped communication.

## How It Works
MUD-style simulation: rooms are graph nodes, agents traverse rooms, gauges monitor state, scoped communication manages information flow.

## What It's For
- Fleet simulation and testing
- Multi-agent scenario modeling

## Who Would Use It
- Multi-agent system researchers
- Simulation engineers

## Language/Stack
- **Primary language:** Cuda

## Status Assessment
**Early stage or stub.**

## Honest Assessment
16K rooms and 65K agents on GPU is impressive. Warp-level combat makes this as much GPU experiment as simulation tool.
