# proof-game-sync

## Intention
⚒️ Float vs Constraint Theory: Cross-platform game state sync. Bit-identical results across platforms.

## How It Works
Cross-platform game state synchronisation: float drift vs constraint-theory snap proof-game-sync is a deterministic simulation benchmark that demonstrates why raw IEEE-754 floating-point arithmetic causes multiplayer game desync across platforms — and how constraint_theory_core::PythagoreanManifold eliminates the drift by projecting state onto a deterministic rational lattice after every game tick. The proof-of-concept simulates 10 entities (position + velocity in ℝ³) over 10 000 ticks at 60 fps, running the same simulation on three "platforms" (Windows, macOS, Linux) that each inject sub-nanometre-per-second velocity perturbations mimicking real-world FPU rounding differences between compilers and CPU microarchitectures.

## What It's For
⚒️ Float vs Constraint Theory: Cross-platform game state sync. Bit-identical results across platforms.

## Who Would Use It
Rust developers

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 9,222 characters, 236 lines
- Code examples: 11 blocks
- Installation instructions: yes
- Testing mentioned: yes
- License mentioned: no
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (11 code blocks)
- Installation/usage instructions provided
- Testing mentioned
- Solid README with good coverage

**Concerns:**
- None immediately apparent from README alone

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
