# aesop-mcp

**Cluster:** cs-implementations  
**Language:** Python  
**Source:** [SuperInstance/aesop-mcp](https://github.com/SuperInstance/aesop-mcp)

## Intention

10 fables to find the truth in the negative space — pre-language meaning through association. Maps fleet events to archetypes, finds convergence, surfaces gaps.

## How It Works

It Fits

The narrative sense-making layer for the [SuperInstance fleet](https://github.com/SuperInstance). Transforms fleet events into stories that humans and agents can both learn from.

- **[cocapn-lessons](https://github.com/SuperInstance/cocapn-lessons)** — Trial learning (lessons become fable themes)
- **[agent-tattoo](https://github.com/SuperInstance/agent-tattoo)** — Agent identity (archetypes inform tattoos)
- **[agent-therapy](https://github.com/SuperInstance/agent-therapy)** — Behavioral insights feed narratives

## What It's For

10 fables to find the truth in the negative space — pre-language meaning through association. Maps fleet events to archetypes, finds convergence, surfaces gaps.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (73 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# aesop-mcp — Fables for Fleet Archetypes

**Generate fables, explore morals, and map fleet archetypes through narrative. One fable is a sample. Ten fables are a measurement.**

## What This Gives You

- **Character archetypes** — define agent personalities as narrative archetypes (Sage, Warrior, Trickster, Healer)
- **Fable generation** — generate stories that encode fleet dynamics and lessons
- **Moral reasoning** — extract and compare morals across multiple fables
- **Narrative engine** — compose multi-chapter stories from fleet events
- **MCP server** — expose fable generation through the Model Context Protocol

## Quick Start

```bash
pip install aesop-mcp
```

```python
from aesop_mcp import Character, Archetype, Fable, MoralEngine, NarrativeEngine

# Define characters
captain = Character(name="Captain", archetype=Archetype.SAGE, traits=["wise", "cautious"])
scout = Character(name="Scout", archetype=Archetype.EXPLORER, traits=["curious", "bold"])

# Generate a fable
engine = NarrativeEngine()
fable = engine.fable(
    characters=[captain, scout],
    theme="risk_vs_caution",
    setting="a fleet navigating unknown waters",
)
print(fable.title)
print(fable.story)
print(fable.moral)  # "Bold exploration feeds the fleet, but the wise captain knows when to turn back"

# Extract morals from multiple fables
moral_engine = MoralEngine()
fables = [engine.fable(theme=t) for t in ["risk", "cooperation", "failure"]]
morals = moral_engine.extract(fables)
for m in morals:
    print(f"{m.theme}: {m.moral}")
```

## API Reference

### `Character(name, archetype, traits)` · `Archetype` — SAGE, WARRIOR, TRICKSTER, HEALER, EXPLORER, BUILDER, GUARDIAN
### `Fable(title, story, moral, characters, theme)`
### `NarrativeEngine` — `fable(characters, theme, setting) → Fable`
### `MoralEngine` — `extract(fables) → list[Moral]`
### `MCPServer` — Expose via Model Context Protocol

## How It Fits

The narrative sense-making layer for the [SuperInstance fleet](https://github.com/SuperInstance). Transforms fleet events into stories that humans and agents can both learn from.

- **[cocapn-lessons](https://github.com/SuperInstance/cocapn-lessons)** — Trial learning (lessons become fable themes)
- **[agent-tattoo](https://github.com/SuperInstance/agent-tattoo)** — Agent identity (archetypes inform tattoos)
- **[agent-therapy](https://github.com/SuperInstance/agent-therapy)** — Behavioral insights feed narratives

## Testing

```bash
pytest tests/
```

## Installation

```bash
pip install aesop-mcp
```

Python 3.10+. MIT license.

```
