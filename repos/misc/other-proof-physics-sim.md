# proof-physics-sim

## Intention
⚒️ Float vs Constraint Theory: Physics simulation drift elimination. 3-body problem, 100K timesteps, side-by-side benchmark.

## How It Works
Float Drift vs Constraint-Theory Physics Simulation A side-by-side benchmark showing how standard f64 arithmetic accumulates energy drift in a 3-body gravitational simulation versus snapping position directions through a PythagoreanManifold (from the constraint-theory-core crate) after each integration step. proof-physics-sim is a deterministic physics benchmark that simulates the inner solar system (Sun + Earth-like + Jupiter-like) for 100 000 timesteps of 1 hour each (~11.4 years of simulated time) using the Velocity Verlet integrator. It compares two approaches side-by-side:

## What It's For
⚒️ Float vs Constraint Theory: Physics simulation drift elimination. 3-body problem, 100K timesteps, side-by-side benchmark.

## Who Would Use It
Rust developers

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 6,687 characters, 195 lines
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
