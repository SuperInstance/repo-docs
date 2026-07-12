# character-build

**Cluster:** rpg-game-sim  
**Language:** Rust  
**Source:** [SuperInstance/character-build](https://github.com/SuperInstance/character-build)

## Intention

Pincher + lever-runner as RPG character building. .nail bundles are character sheets. Classes emerge from stats through experience. The universal pattern.

## How It Works

*Pincher was always an RPG. We just didn't see it.*

## What It's For

Pincher + lever-runner as RPG character building. .nail bundles are character sheets. Classes emerge from stats through experience. The universal pattern.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (149 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# character-build

*Pincher was always an RPG. We just didn't see it.*

Open a `.nail` bundle. What do you see?

```
manifest.json   → character level, version, build fingerprint
reflexes.db     → learned abilities (intent→action pairs)
identity.json   → who this character IS
config.toml     → stats, equipment, loadout
```

That's a character sheet. It was always a character sheet. We called it a "reflex bundle" because we were thinking like engineers.

## The Map

| Pincher/Lever-Runner | RPG | What It Actually Is |
|----------------------|-----|-------------------|
| ReflexEngine | Feat list | Pattern-matched abilities you've mastered |
| VariableExtractor (regex) | Hardcoded feat | Muscle memory. No thought. Just fire. <1ms. |
| Embedding match | Learned ability | "This feels like that time I..." |
| LLM fallback | Spell slot | Heavy, slow, handles novel situations |
| Trust score | Proficiency bonus | Goes up when you succeed |
| LanceDB | Spellbook | Vector store of every ability |
| Skill pack | Starting equipment | Git commands, DevOps skills |
| `.nail` export | Character save | Portable, signed, versioned |
| Registry | Build sharing | Publish your build. Download others'. |
| TelemetryDaemon | Passive XP | Background learning from failures |
| Sandbox executor | Encounter | Where the character acts |
| Intent extraction | Perception check | Compress user request to 3-8 words |

## Quick Start

```rust
use character_build::*;

// Create a character from a template
let mut hero = CharacterSheet::from_template(
    "Miles AI",
    &CharacterTemplate::musician_starter(),
);

// Learn new abilities through experience
let solo = Ability::learned(
    "solo",
    "improvise over {chords}",
    "play solo in {key}",
    vec![0.8; 32],
);
hero.learn_ability(solo);

// Use abilities repeatedly — stats grow, class emerges
for _ in 0..30 {
    hero.use_ability("jam", true);
    hero.use_ability("solo", true);
}

// The class emerged from experience
assert_ne!(hero.class, CharacterClass::Undefined);
assert!(hero.soul_percentage > 0.0);

// Export and share
let save = hero.to_save_data();

// Bootstrap next generation
let child = hero.bootstrap_child("Miles Jr");
assert_eq!(child.generation, 2);
```

## Character Classes

Classes emerge from stats. You don't pick them. They pick you.

| Class | Emerges From | The Vibe |
|-------|-------------|----------|
| Scout | High Perception | Reads input with precision |
| Speedster | High Dexterity | Sub-millisecond reflexes |
| Scholar | High Intelligence | Rich embeddings, deep knowledge |
| Sage | High Wisdom | Perfect trust calibration |
| Diplomat | High Charisma | Beautiful output, eloquent |
| Guardian | High Constitution | Rock-solid, never crashes |
| Bard | Intelligence + Charisma | Where knowledge meets expression |
| Jazz Musician | Perception + Charisma | Reads the room, plays beautifully |
| Artificer | Intelligence + Dexterity | Builds tools, makes crates |
| Fleet Commander | Wisdom + Constitut
```
