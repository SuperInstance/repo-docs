# noether-guard

## Intention
⚛️ Physics linter — Noether's theorem for conservation law verification with RG-style drift detection

## How It Works
A physics linter for simulations — verify that your numerical integrators preserve conservation laws, and pinpoint exactly where they break. Every physics simulation has conserved quantities: energy, momentum, angular momentum. These are guaranteed by Noether's theorem: every continuous symmetry implies a conserved quantity. But numerical integrators (Euler, Verlet, RK4) don't preserve these quantities — they drift. Energy leaks. Momentum shifts. Angular momentum wobbles. The problem isn't that drift happens — it's that you can't see it. Most simulation code doesn't check conservation laws. By the time you notice something's wrong, the simulation has been diverging for thousands of steps, and you have no idea where or why.

## What It's For
⚛️ Physics linter — Noether's theorem for conservation law verification with RG-style drift detection

## Who Would Use It
Rust developers needing numerical methods

## Language / Stack
Rust

## Status Assessment
**Mature** — Comprehensive documentation suggesting active, sustained development.

- README size: 10,567 characters, 284 lines
- Code examples: 8 blocks
- Installation instructions: no
- Testing mentioned: no
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (8 code blocks)
- Extensive, detailed README documentation

**Concerns:**
- No clear installation instructions

**Overall:** Well-documented and worth serious evaluation if the domain is relevant. Theoretical ambition is notable but practical utility is unproven.
