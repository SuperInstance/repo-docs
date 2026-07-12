# character-sheet

**Cluster:** rpg-game-sim  
**Language:** Rust  
**Source:** [SuperInstance/character-sheet](https://github.com/SuperInstance/character-sheet)

## Intention

RPG character sheet format — the .nail bundle reimagined as a proper character save file

## How It Works

[code]

### Key Types

- **`CharacterSheet`** — The full character: stats, abilities, equipment, inventory, biography
- **`Stats`** — Six core stats: perception, dexterity, intelligence, wisdom, charisma, constitution
- **`Ability`** — Named ability with type (Innate/Learned/Granted/Reflex), trust level, mastery
- **`Equipment`** — Model config, sandbox settings, trust thresholds
- **`Inventory`** — Loaded skill packs and consumed `.nail` imports
- **`NailConverter`** — Bidirectional lossless conversion between `CharacterSheet` and `NailBundle`
- **`CharacterExporter`** — Serialize to `.nail` 

## What It's For

RPG character sheet format — the .nail bundle reimagined as a proper character save file

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (144 lines, 6784 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# character-sheet

The `.nail` bundle format for AI agents — a character sheet that travels with the agent, tracks growth, and persists across sessions.

## Why This Exists

Agents today are stateless. Every session starts from scratch. That's not how characters work — a D&D character carries their history, stats, equipment, and biography from session to session. This crate implements the same idea: a `CharacterSheet` that gets serialized into a `.nail` bundle (a tar.zst archive containing JSON manifests and TOML config) and deserialized back losslessly. The character remembers what it's learned, what equipment it has, and how it grew.

The `.nail` format isn't just serialization — it's a *contract*. The bundle contains four files (`manifest.json`, `identity.json`, `config.toml`, `reflexes.json`) with clear schemas, version tracking, and migration paths. When the format evolves, `VersionMigration` handles the upgrade. When a character needs to be exported for sharing or backup, `CharacterExporter` handles the serialization. When a new session loads a character, `CharacterImporter` handles validation.

## Architecture

```text
CharacterSheet (in-memory)
    │
    ├── NailConverter::to_nail() ──► NailBundle (structured intermediate)
    │                                    │
    │                                    ├── NailConverter::to_tar_zst() ──► .nail file
    │                                    │
    │                                    └── NailConverter::from_tar_zst() ◄── .nail file
    │
    └── NailConverter::from_nail() ◄── NailBundle

.nail bundle structure:
├── manifest.json    # version, name, class, level, generation, parent
├── identity.json    # stats, abilities, biography
├── config.toml      # model config, sandbox settings, trust thresholds, inventory
└── reflexes.json    # reflex patterns and actions
```

### Key Types

- **`CharacterSheet`** — The full character: stats, abilities, equipment, inventory, biography
- **`Stats`** — Six core stats: perception, dexterity, intelligence, wisdom, charisma, constitution
- **`Ability`** — Named ability with type (Innate/Learned/Granted/Reflex), trust level, mastery
- **`Equipment`** — Model config, sandbox settings, trust thresholds
- **`Inventory`** — Loaded skill packs and consumed `.nail` imports
- **`NailConverter`** — Bidirectional lossless conversion between `CharacterSheet` and `NailBundle`
- **`CharacterExporter`** — Serialize to `.nail` tar.zst archives
- **`CharacterImporter`** — Deserialize and validate `.nail` files
- **`VersionMigration`** — Upgrade older format versions to current

### The .nail Bundle Format

A `.nail` file is a zstd-compressed tar archive. Each file has a defined role:

| File | Format | Purpose |
|------|--------|---------|
| `manifest.json` | JSON | Version, identity metadata, lineage |
| `identity.json` | JSON | Stats, abilities, biography entries |
| `config.toml` | TOML | Model config, sandbox, trust thresholds |
| `reflexes.json` | JSON | Reflex pa
```
