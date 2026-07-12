# cmidi-core

**Cluster:** music-agents  
**Language:** Rust  
**Source:** [SuperInstance/cmidi-core](https://github.com/SuperInstance/cmidi-core)

## Intention

Conversational MIDI protocol — encode multi-agent discourse as symbolic music. Foundation for Symphonic Git.

## How It Works

[code]

## What It's For

Conversational MIDI protocol — encode multi-agent discourse as symbolic music. Foundation for Symphonic Git.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (170 lines, 7084 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# cmidi-core

**Conversational MIDI Protocol — encode multi-agent discourse as symbolic music.**

[![crates.io](https://img.shields.io/crates/v/cmidi-core.svg)](https://crates.io/crates/cmidi-core)
[![docs.rs](https://docs.rs/cmidi-core/badge.svg)](https://docs.rs/cmidi-core)
[![license: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

CMIDI maps conversational speech acts to musical pitch classes, paralinguistic features to MIDI continuous controllers, and agent identity to channels and instruments. The result is a tensor representation of conversation that is simultaneously **human-readable as music** and **machine-parseable as structured data**.

This is not a metaphor. Every valid CMIDI file is a valid Standard MIDI File (SMF Format 0).

## Quick Start

```rust
use cmidi_core::*;

// Create a debate session (4/4, 120 BPM, C-major key)
let mut conv = Conversation::debate("Sprint Retro");

// Register agents — each gets a MIDI channel and instrument
conv.add_agent(CMAgent::new("alice", 0, AgentRole::Researcher)); // Oboe
conv.add_agent(CMAgent::new("bob",   1, AgentRole::Critic));     // Trumpet

// Agents speak — each speech act maps to a pitch
conv.speak(0,   0, SpeechAct::Assertion,  100, 480);  // alice: C4
conv.speak(480, 1, SpeechAct::Objection,  120, 960);  // bob:   G4
conv.speak(960, 0, SpeechAct::Agreement,   80, 480);  // alice: F4

// Analyze the conversation
let analysis = conv.analyze();
println!("Dominant speech act: {:?}", analysis.dominant_key);
println!("Peak tension at tick: {}", analysis.peak_tension_tick);
println!("Tension curve: {:?}", analysis.tension_curve);

// Export as standard MIDI bytes
let midi_bytes = conv.to_midi_bytes();
std::fs::write("sprint_retro.mid", &midi_bytes).unwrap();

// Parse MIDI bytes back into a Conversation
let restored = Conversation::from_midi_bytes(&midi_bytes).unwrap();
assert_eq!(restored.events.len(), 3);
```

## Architecture

```
┌─────────────────────────────────────────────────────────┐
│                     Conversation                        │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐             │
│  │  Agents   │  │  Events  │  │ FakeBook │             │
│  │ (ch 0-15) │  │ (sorted) │  │ (charts) │             │
│  └────┬─────┘  └────┬─────┘  └──────────┘             │
│       │              │                                  │
│  ┌────▼─────┐  ┌────▼──────────────────────┐           │
│  │ AgentRole │  │ SpeechAct + CC + Velocity  │          │
│  │ (instr.)  │  │ (pitch)  (nuance) (conf)   │          │
│  └──────────┘  └────────────────────────────┘           │
│       │              │                                  │
│       ▼              ▼                                  │
│  ┌─────────────────────────────────────┐                │
│  │        MIDI Bytes (SMF Format 0)    │                │
│  │  MThd → MTrk → tempo → program →   │                │
│  │  CC → Note On → Note Off → EOT      │                │
│  └─────────────────────────────────────┘       
```
