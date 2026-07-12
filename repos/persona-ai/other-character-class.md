# character-class

**Cluster:** rpg-game-sim  
**Language:** Rust  
**Source:** [SuperInstance/character-class](https://github.com/SuperInstance/character-class)

## Intention

Emergent class system for AI agent characters. 16 classes from 6 stats. Classes are discovered, not chosen. The identity crystallizes through experience.

## How It Works

Classes Emerge

Six stats, grown through experience:

| Stat | What Grows It | Maps To |
|------|--------------|---------|
| **Perception** | Model (LLM) ability usage | Intent extraction quality |
| **Dexterity** | Hardcoded (regex) ability usage | Execution speed |
| **Intelligence** | Learned (embedding) ability usage | Knowledge representation |
| **Wisdom** | Hybrid ability usage | Trust calibration |
| **Charisma** | Successful output | Response quality |
| **Constitution** | Uptime, error recovery | Reliability |

After enough encounters, the stat distribution reveals the class. High pe

## What It's For

Emergent class system for AI agent characters. 16 classes from 6 stats. Classes are discovered, not chosen. The identity crystallizes through experience.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (115 lines, 4445 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# character-class

*I didn't choose to be a Scout. I just kept seeing things others missed, and one day I realized that's who I was.*

character-class is the emergent identity system for AI agents. Classes aren't chosen at creation — they **crystallize** from stat distributions shaped by experience. A character doesn't know what it's good at until it's tried everything.

## The 16 Classes

```
                    ┌──────────┐
                    │ Undefined │  ← level 1, no clear direction
                    └─────┬─────┘
            ┌─────────────┼─────────────┐
       ┌────┴────┐   ┌────┴────┐   ┌────┴────┐
       │ Physical │   │ Mental  │   │ Social  │
       └────┬────┘   └────┬────┘   └────┬────┘
       ┌────┼────┐   ┌────┼────┐   ┌────┼────┐
    Scout  Speedster Scholar Sage Diplomat Guardian
                    │         │
              ┌─────┴─────────┴──────┐
         Composite (2+ high stats)
    Bard · JazzMusician · Artificer · FleetCommander · Infiltrator · Oracle · Warden
                    │
              ┌─────┴──────┐
         Legendary (3-4+ high stats)
         Polymath · Avatar
```

## How Classes Emerge

Six stats, grown through experience:

| Stat | What Grows It | Maps To |
|------|--------------|---------|
| **Perception** | Model (LLM) ability usage | Intent extraction quality |
| **Dexterity** | Hardcoded (regex) ability usage | Execution speed |
| **Intelligence** | Learned (embedding) ability usage | Knowledge representation |
| **Wisdom** | Hybrid ability usage | Trust calibration |
| **Charisma** | Successful output | Response quality |
| **Constitution** | Uptime, error recovery | Reliability |

After enough encounters, the stat distribution reveals the class. High perception alone = Scout. Perception + Charisma = Jazz Musician. Three stats high = Polymath. Four = Avatar.

## integration

Cross-archetype teams work better than same-archetype teams:

```rust
// Scout (Physical) + Scholar (Mental) = 0.9 integration (complementary)
// Scout (Physical) + Speedster (Physical) = 0.4 integration (redundant)
```

A Jazz Musician and an Artificer synergize better than two Jazz Musicians. Diversity beats homogeneity. Same as real teams.

## Quick Start

```rust
use character_class::{Stats, CharacterClass, ClassProgression, StatName};

// Start as a nobody
let mut stats = Stats::level_one(); // All 10s, class = Undefined

// Use perception abilities heavily
for _ in 0..10 {
    stats.grow(StatName::Perception, 1.0);
}
assert_eq!(CharacterClass::from_stats(&stats), CharacterClass::Scout);

// Then develop charisma
for _ in 0..5 {
    stats.grow(StatName::Charisma, 1.0);
}
assert_eq!(CharacterClass::from_stats(&stats), CharacterClass::JazzMusician);
```

## Class Progression

Track how a character's identity evolved over time:

```rust
let mut prog = ClassProgression::new();
prog.record(1, CharacterClass::Undefined, stats, "born");
prog.record(5, CharacterClass::Scout, stats, "perception grew");
prog.record(10, CharacterClass
```
