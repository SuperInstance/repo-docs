# lau-onboarding

## Intention

6-phase ensign orientation. Room config → story → assignment → baton.

## How It Works

A new agent doesn't know anything about the room it's been assigned to. The onboarding engine walks it through six phases:
1. **Identity** — Who am I? What type of agent am I?
2. **Orientation** — What room am I in? What controls are available?
3. **Briefing** — What's the deadband situation? What's my margin?
4. **Story Building** — What happened before I arrived? Rewind the automation history.
5. **Assignment** — What's my first task? Who's my supervisor?
6. **Ready** — Hand off the baton to the ensign system.
Each phase produces structured output that feeds into the next. The engine tracks progress and can resume from any phase.

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. 6-phase ensign orientation. Room config → story → assignment → baton.

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (82 lines), includes examples.

- README length: 106 lines, 3640 characters
- Documented sections: The concept in 60 seconds, Quick start, Key types, Pre-built room configs, Phase details

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with reasonable detail. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
