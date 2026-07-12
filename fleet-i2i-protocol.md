# fleet-i2i-protocol

**URL:** https://github.com/SuperInstance/fleet-i2i-protocol

## Intention
Inter-agent messaging protocol (I2I) — text-based 'bottles' with speech-act semantics, capability discovery, and group routing. The nervous system of the fleet.

## How It Works
Rust implementation of an SMTP-inspired protocol where agents exchange structured text messages. Each message is an envelope with From/To/CC/Reply-To headers and typed payloads (speech acts, capabilities, etc.). Transport-agnostic (files, HTTP, WebSocket, in-memory).

## What It's For
Agent-to-agent communication — coordination, negotiation, information sharing.

## Who Would Use It
Multi-agent system developers.

## Language/Stack
Rust

## Status Assessment
Active — well-designed protocol with parser, serializer, and transport abstractions.

## Honest Assessment
Real project — genuinely thoughtful protocol design inspired by email/SMTP. One of the more substantive repos.
