# character-library

**Cluster:** rpg-game-sim  
**Language:** Python  
**Source:** [SuperInstance/character-library](https://github.com/SuperInstance/character-library)

## Intention

Library for managing character data.

## How It Works

### Package Structure

[code]

## What It's For

Library for managing character data.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (335 lines, 8994 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# Character Library

**Comprehensive Personality Modeling System for AI Characters**

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-beta-orange.svg)]()

A standalone Python package for creating psychologically-grounded AI characters with rich personalities, emotional modeling, skill development, and dynamic relationships.

## Features

### Personality Frameworks
- **Big Five (OCEAN)**: Openness, Conscientiousness, Extraversion, Agreeableness, Neuroticism
- **Enneagram**: 9 personality types with core motivations and fears
- **MBTI**: 16 personality types with cognitive functions

### Character Archetypes
12 pre-configured archetypes with unique personalities:
- **The Innovator** - Creative visionary who pushes boundaries
- **The Educator** - Patient teacher who inspires learning
- **The Storyteller** - Wise narrator who connects through stories
- **The Creator** - Artistic visionary who brings beauty to life
- **The Philosopher** - Deep thinker who seeks fundamental truths
- **The Analyst** - Rigorous investigator who pursues truth
- **The Leader** - Charismatic guide who unites and inspires
- **The Moral Guide** - Ethical compass who shows the right path
- **The Humorist** - Witty spirit who brings joy through laughter
- **The Empath** - Compassionate listener who heals through understanding
- **The Builder** - Practical visionary who constructs lasting foundations
- **The Engineer** - Systems thinker who solves complex technical challenges

### Emotional Modeling
- 8 basic emotions (Joy, Trust, Fear, Surprise, Sadness, Disgust, Anger, Anticipation)
- Multi-dimensional emotional states (intensity, valence, arousal)
- Visible emotional expressions and cues
- Emotional transitions and decay

### Relationship Dynamics
- 8 relationship types (Friendship, Mentorship, Rivalry, Romantic, etc.)
- Compatibility analysis between characters
- Relationship strength and trust tracking
- Shared history and conflict management

### Skill Development
- Skill trees with prerequisites and specializations
- Experience-based progression
- Mastery levels (Novice to Grandmaster)
- Skill usage tracking

## Installation

### Basic Installation
```bash
pip install character-library
```

### With Agent Integration (requires hierarchical-memory)
```bash
pip install character-library[agent]
```

### From Source
```bash
git clone https://github.com/luciddreamer/character-library.git
cd character-library
pip install -e .
```

## Quick Start

### Creating a Character

```python
from character_library import CharacterLibrary, CharacterArchetype

# Create character library
library = CharacterLibrary()

# Create a character from an archetype
character = library.create_character(CharacterArchetype.INNOVATOR)

# Access personality traits
print(character.name)  # "Dr. Aria Starweaver"
print(character.b
```
