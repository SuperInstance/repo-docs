# chess-engine

**Cluster:** constraint-theory  
**Language:** Rust  
**Source:** [SuperInstance/chess-engine](https://github.com/SuperInstance/chess-engine)

## Intention

Rust chess engine (forked from vdmo/chess) — transposition table patterns for guard2mask CSP solver

## How It Works

[code]

### Key Design Decisions

**Bitboards over arrays:** All piece positions stored as `u64` bitmasks for fast move generation.

**Make/unmake over copy-make:** Position state is modified in-place with undo stack for efficiency.

**Ray-based sliding moves:** No magic bitboards yet—simple ray-walking for correctness-first development.

**Separate binaries:** Engine (`vdmo`) and GUI (`vdmo-chess-gui`) share the library crate.

## What It's For

Rust chess engine (forked from vdmo/chess) — transposition table patterns for guard2mask CSP solver

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (262 lines, 6873 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# VDMO Chess Engine


## Meta

**Domain:** tools
**Depends on:** —
**Depended by:** —
**Implements:** Rust chess engine (forked from vdmo/chess) — transposition table patterns for gu...
**Related:** —


A chess engine written in Rust with a focus on correctness and clarity.

## Features

### ✅ Implemented

- **Bitboard representation** for efficient board state
- **Full move generation** for all pieces (pawns, knights, bishops, rooks, queens, king)
- **Special moves**: castling (king-side and queen-side), en-passant, promotions
- **Make/unmake** with state stack for efficient search
- **Attack detection** for all piece types (used in legality checking)
- **Perft** (performance test) for move generation validation
- **Alpha-beta search** with:
  - Iterative deepening
  - Quiescence search (tactical extensions)
  - Mate detection
  - **Late Move Reductions (LMR)** for efficient deep search
  - **Null-Move Pruning** for forward pruning
- **Transposition table** with Zobrist hashing (1M entries)
- **Advanced move ordering**:
  - TT move (transposition table best move first)
  - MVV-LVA (Most Valuable Victim - Least Valuable Attacker) for captures
  - Killer moves (2 killers per ply)
  - History heuristic (move success tracking)
- **Enhanced evaluation**:
  - Material counting
  - Piece-square tables for all pieces
  - Positional understanding
- **Time management**:
  - Classical time controls (wtime/btime/winc/binc)
  - Move time controls (movetime)
  - Moves-to-go support
  - Adaptive time allocation
- **UCI protocol** support for GUI integration
- **Native GUI** (`vdmo-chess-gui.exe`) using egui/eframe

### 🚧 To Be Implemented

- Counter moves and follow-up moves
- More evaluation features (pawn structure, king safety, mobility)
- Aspiration windows
- Principal variation (PV) extraction and display
- Opening book
- Endgame tablebases
- NNUE evaluation (long-term goal)

## Building

### Requirements

- Rust 1.70+ ([install here](https://rustup.rs/))

### Build Commands

```bash
# Build release (optimized)
cargo build --release

# Build both binaries
cargo build --release --bin vdmo            # Engine
cargo build --release --bin vdmo-chess-gui  # GUI
```

Binaries will be in `target/release/`:
- `vdmo.exe` - UCI engine
- `vdmo-chess-gui.exe` - Graphical interface

## Usage

### 1. Perft (Move Generation Testing)

Validate move generation correctness:

```bash
# Test from starting position
cargo run --release --bin vdmo -- perft 5

# Test from custom FEN
cargo run --release --bin vdmo -- perft 4 "rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1"
```

**Expected perft values from startpos:**
- Depth 1: 20
- Depth 2: 400
- Depth 3: 8,902
- Depth 4: 197,281
- Depth 5: 4,865,609

### 2. UCI Mode (Chess GUIs)

Run as a UCI engine:

```bash
cargo run --release --bin vdmo -- uci
```

Then interact via stdin:
```
uci
isready
position startpos moves e2e4 e7e5
go depth 6
# or with time controls:
go wtime 300000 btime 300000 winc 2000 binc 2000
# or wit
```
