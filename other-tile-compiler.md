# tile-compiler

## Intention
Compile game strategies into fast lookup tables via tile-based field training

## How It Works
**Tile Compiler** trains game-playing policies via tile-based Monte Carlo field training, then compiles them into zero-dependency lookup tables. It supports the full pipeline: define a game, train a tile field via self-play, compile to a `CompiledPolicy`, optimize for speed, factorize for memory efficiency, and generate JIT-compiled policies. Built-in games include Tic-Tac-Toe, Connect Four, and extensible protocol-based game definitions.

The README includes code examples and API documentation.

Key topics: ternary math, conservation laws, neural networks

## What It's For
Neural network or machine learning computation.

## Who Would Use It
Python developers, AI/ML practitioners

## Language / Stack
- **Language:** Python
- **Dependencies:** Zero/stdlib only
- **Published:** GitHub only

## Status Assessment
Well-documented — likely functional

## Honest Assessment
No test count mentioned in README — implementation depth unclear. Prides itself on zero dependencies, which is good for a library but limits integration. Not published to any package registry — GitHub-only. Lacks installation instructions — may be difficult to get started.

## README Length
4488 characters
