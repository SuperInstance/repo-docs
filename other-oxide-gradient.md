# oxide-gradient

## Intention
Experiment: gradient-based GPU resource optimization via ternary search. Ternary {-1,0,+1} as gradient directions for block size, shared mem

## How It Works
Gradient-based GPU resource optimization via ternary search. GPU kernel performance is a function of three parameters: block size (threads per block), shared memory allocation, and warp count. The search space is small enough that you don't need full autotuning frameworks — you need a disciplined search that converges in  Self - simulate_occupancy(&mut self) — compute occupancy from SM shared memory limits and warp limits - new(params: KernelParams) -> Self — initialize with starting parameters - step() -> f64 — one optimization step, returns execution time - search(steps: usize) -> Vec — run N steps, returns convergence curve - apply_gradient() — apply current gradient to get next parameters - best_time() -> f64 / steps_taken() -> usize / improvements() -> usize

## What It's For
Experiment: gradient-based GPU resource optimization via ternary search. Ternary {-1,0,+1} as gradient directions for block size, shared mem

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 6,048 characters, 150 lines
- Code examples: 6 blocks
- Installation instructions: no
- Testing mentioned: yes
- License mentioned: no
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (6 code blocks)
- Testing mentioned
- Solid README with good coverage

**Concerns:**
- No clear installation instructions
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
