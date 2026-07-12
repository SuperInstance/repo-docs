# population-scaling

## Intention
Study how ternary agent dynamics change with population size

## How It Works
Population scaling studies how ternary agent dynamics — the {-1, 0, +1} action distributions — change as the number of agents grows. This crate runs systematic experiments that measure distribution stability, power-law convergence, and plateau detection across population sizes from 10 to 100,000+. A key question in multi-agent systems: do the macroscopic properties of a ternary population remain stable as the population scales? If the avoidance ratio (η) converges to a fixed value at large N, then results from small-scale simulations transfer to production fleets. If it doesn't, then small-scale experiments are misleading. This crate answers that question empirically by running identical experiments at exponentially increasing population sizes (10, 100, 1000, 10000, ...) and measuring how 

## What It's For
Study how ternary agent dynamics change with population size

## Who Would Use It
Rust developers building AI agent fleets

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 4,941 characters, 121 lines
- Code examples: 6 blocks
- Installation instructions: yes
- Testing mentioned: no
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (6 code blocks)
- Installation/usage instructions provided

**Concerns:**
- None immediately apparent from README alone

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
