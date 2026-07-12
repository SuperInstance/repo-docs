# character-encounter

**Cluster:** rpg-game-sim  
**Language:** Rust  
**Source:** [SuperInstance/character-encounter](https://github.com/SuperInstance/character-encounter)

## Intention

RPG encounter engine — the runtime where character sheets (.nail bundles) come alive

## How It Works

[code]

### Key Types

- **`Encounter`** — A single user request with context, timestamp, and extracted intent
- **`EncounterEngine`** — The main loop: perception → difficulty → ability → roll → rewards
- **`PerceptionCheck`** — Extracts intent from raw text; quality depends on perception stat
- **`AbilityResolution`** — Four-tier ability matcher (hardcoded → learned → hybrid → model)
- **`DifficultyAssessment`** — Auto-scales difficulty based on how well abilities cover the intent
- **`CharacterSheet`** — The persona: stats, abilities, trust, level, XP, encounter log
- **`EncounterLog`** — Fu

## What It's For

RPG encounter engine — the runtime where character sheets (.nail bundles) come alive

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (153 lines, 7263 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# character-encounter

RPG encounter engine that transforms agent interactions into stat-based ability checks with trust, XP, and leveling.

## Why This Exists

Most agent frameworks treat every request identically — same latency path, same confidence, same cost. That's wrong. An agent that's handled a thousand greetings shouldn't process them the same way it handles a novel request it's never seen. This crate borrows from RPG game design: every interaction is an *encounter* resolved through ability checks, perception rolls, and trust-weighted probability. The result is a character that visibly grows — leveling up abilities it uses often, building trust through success, and degrading through failure.

The key insight: **ability resolution is a tiered fallback system**. Hardcoded regex matches fire in microseconds. Learned embedding matches fire in under a millisecond. Only truly novel requests fall through to expensive LLM calls. This isn't optimization — it's the architecture.

## Architecture

```text
Input Text
    │
    ▼
PerceptionCheck ─── extract intent (stat-based roll)
    │
    ▼
DifficultyAssessment ─── how many abilities match?
    │
    ▼
AbilityResolution ─── hardcoded → learned → hybrid → model
    │                       (0ms)   (<1ms)   (1ms)   (500ms)
    ▼
Trust-weighted Roll ─── success/failure probability
    │
    ▼
XP & Trust Updates ─── character grows
    │
    ▼
EncounterLog ─── full history, biography generation
```

### Key Types

- **`Encounter`** — A single user request with context, timestamp, and extracted intent
- **`EncounterEngine`** — The main loop: perception → difficulty → ability → roll → rewards
- **`PerceptionCheck`** — Extracts intent from raw text; quality depends on perception stat
- **`AbilityResolution`** — Four-tier ability matcher (hardcoded → learned → hybrid → model)
- **`DifficultyAssessment`** — Auto-scales difficulty based on how well abilities cover the intent
- **`CharacterSheet`** — The persona: stats, abilities, trust, level, XP, encounter log
- **`EncounterLog`** — Full encounter history with filtering and biography generation

### Ability Resolution Tiers

| Tier | Type | Latency | When It Fires |
|------|------|---------|---------------|
| 1 | `Hardcoded` | ~0ms | Regex pattern match |
| 2 | `Learned` | <1ms | Embedding cosine similarity ≥ threshold |
| 3 | `Hybrid` | ~1ms | Regex OR embedding match |
| 4 | `Model` | ~500ms | Fallback for novel requests |

### Difficulty & Rewards

| Difficulty | XP Multiplier | Trust Reward | Trust Penalty | When |
|-----------|---------------|--------------|---------------|------|
| Easy | 1.0× | +0.5 | −5.0 | Hardcoded match |
| Medium | 1.5× | +1.5 | −3.0 | Low-confidence learned match |
| Hard | 2.5× | +3.0 | −1.5 | Hybrid match |
| Novel | 5.0× | +5.0 | −0.5 | Model fallback only |

Novel encounters penalize trust the least — you shouldn't be punished for not knowing something. But they reward the most when you succeed.

## Usage

```rust
use chara
```
