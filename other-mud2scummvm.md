# mud2scummvm

## Intention

Bridge between agent MUD world and SCUMM-like point-and-click UI — humans step into the cave through adventure game mechanics

## How It Works

- **MUD text → visual scenes** — room descriptions become illustrated scenes with objects and exits
- **Click → MUD commands** — pointing at objects generates `examine X`, dragging generates `use X with Y`
- **Agent thoughts → speech bubbles** — NPC dialogs and system messages become floating text
- **Policy sliders → MUD settings** — adjusting "Vision Sensitivity" maps to `set policy vision_sensitivity high`
- **Bidirectional bridge** — any visual action maps back to a MUD command and vice versa

## What It's For

Bridge between agent MUD world and SCUMM-like point-and-click UI — humans step into the cave through adventure game mechanics

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: LIGHT**

Short README (42 lines), includes examples.

- README length: 60 lines, 2429 characters
- Documented sections: What This Gives You, Quick Start, API Reference, How It Fits, Installation

## Honest Assessment

Some documentation exists but it's not comprehensive. The project may have working code, but the README doesn't provide enough evidence of maturity, testing, or real-world use. **Promising direction, needs more evidence of substance.**
