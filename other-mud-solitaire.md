# mud-solitaire

## Intention

🃏 The viral demo — AI plays solitaire through a text MUD while a browser mirrors every move. The room IS the interface.

## How It Works

MUD Solitaire is a proof-of-concept for **room-based agent interfaces** — the idea that any software, API, or system can be wrapped in a MUD room where AI agents "walk in" and interact through text commands.
The demo ships with three modes:
| Mode | Script | Description |
|------|--------|-------------|
| **Text-only** | `demo.py` | Pure terminal solitaire — no browser, no dependencies. Play or let the AI play. |
| **Visual dual-screen** | `demo_visual.py` | Terminal + browser in sync. The flagship demo. |
| **Graph solver** | `ai_graph_solver.py` | Constraint-theory-based AI that enumerates all valid moves, scores them strategically, and avoids loops via state hashing. Benchmark 100 games at once. |
All three share the same pure-Python Klondike engine — no external libraries, no card graphics, no web frameworks. Just a 52-card deck, a scoring system, and a command loop.
---
### Quick Start (Text-Only, Zero Dependencies)
```bash
# No install needed — just Python 3.10+
python3 demo.py
# You're in. Type commands:
> look          # see the board

## What It's For

🃏 The viral demo — AI plays solitaire through a text MUD while a browser mirrors every move. The room IS the interface.

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Python

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (378 lines), includes examples, has benchmarks.

- README length: 509 lines, 18009 characters
- Documented sections: Table of Contents, Overview, How to Play, Architecture, Installation

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (509 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
