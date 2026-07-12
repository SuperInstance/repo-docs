# Persona AI — Index

**Total repos: 11**

The persona-ai collection implements a full RPG-style character system for AI agents. Characters have stats, classes, skills, equipment, arcs, and encounters — all formalized as data structures that travel with the agent between sessions. The `.nail` bundle format (a tar.zst archive containing JSON manifests and TOML config) is the serialization contract.

## Category Overview

This category reimagines AI agent identity through the lens of tabletop RPG character sheets. Instead of opaque model weights, an agent's personality, capabilities, and growth history are explicit, inspectable, and portable.

### Core System

- **persona-engine** — Full persona decomposition/composition system: extract personality from audio, compose new personas, vibe-code character creation. Fleet-native with rhythmic TTS and I2I integration
- **character-sheet** — The RPG character sheet format. `CharacterSheet` struct with stats, abilities, equipment, inventory, biography. Serializes to `.nail` bundles
- **ai-character-sdk** — SDK for building AI characters programmatically
- **ai-character-integrations** — Integration layer for external systems

### Character Building Blocks

- **character-build** — Character creation and customization flow
- **character-class** — Class system (mage, warrior, rogue, etc.) determining stat growth and abilities
- **character-skill-trees** — Skill tree progression — which abilities unlock which
- **character-arc** — Character development arcs — narrative progression tracking
- **character-encounter** — Encounter system — how characters meet and interact
- **character-library** — Library of pre-built character templates
- **character-agent-integration** — Connecting character sheets to agent runtimes

### The `.nail` Format

The central innovation: a **`.nail` bundle** is a tar.zst archive containing:
- `manifest.json` — Version, metadata, migration info
- `identity.json` — Stats, biography, personality
- `config.toml` — Model config, sandbox settings, trust thresholds
- `reflexes.json` — Learned reflexes and conditioned responses

When a character loads into a new session, the `CharacterImporter` validates the bundle. When the format evolves, `VersionMigration` handles upgrades. When a character needs sharing, `CharacterExporter` handles serialization — losslessly.

### Key Interconnections

- **persona-engine** connects to audio systems (voice decomposition) and TTS (rhythmic speech)
- **character-sheet** uses `.nail` bundles which relate to the broader SuperInstance file format ecosystem
- The RPG metaphor connects to the PLATO/LAU game engine (lau-mathematics category)
- Stats (perception, dexterity, intelligence, wisdom, charisma, constitution) map to agent capability profiles
- Equipment slots model "model config, sandbox settings, trust thresholds" — infrastructure as inventory

## Full Repository Listing

| Repo | Language | Description |
|------|----------|-------------|
| [persona-engine](./other-persona-engine.md) | Python | Full persona engine — decompose, compose, vibe-code |
| [character-sheet](./other-character-sheet.md) | Rust | RPG character sheet → .nail bundle format |
| [ai-character-sdk](./other-ai-character-sdk.md) | TypeScript | AI character SDK |
| [ai-character-integrations](./other-ai-character-integrations.md) | TypeScript | External integrations |
| [character-build](./other-character-build.md) | Rust | Character creation flow |
| [character-class](./other-character-class.md) | Rust | Class system |
| [character-skill-trees](./other-character-skill-trees.md) | Rust | Skill tree progression |
| [character-arc](./other-character-arc.md) | Rust | Narrative arc tracking |
| [character-encounter](./other-character-encounter.md) | Rust | Encounter system |
| [character-library](./other-character-library.md) | Rust | Pre-built templates |
| [character-agent-integration](./other-character-agent-integration.md) | Rust | Agent runtime integration |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
