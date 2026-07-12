# oxide-workflow

## Intention
GPU kernel workflow orchestration with ternary step states. DAG execution, retry on failure, rollback, progress tracking.

## How It Works
DAG-based workflow orchestration for multi-step GPU kernel pipelines with ternary step states, automatic retry on failure, topological ordering (Kahn's algorithm), rollback support, and progress tracking. Each step resolves to a ternary outcome: complete (+1), running (0), or failed (−1). Complex GPU workloads — training pipelines, inference graphs, data processing chains — require orchestration that handles: - Dependencies — kernels that must run in order (e.g., preprocessor → model → postprocessor). - Failure recovery — transient GPU errors (OOM, CUDA faults) need automatic retry with bounded attempts. - Rollback — when a step fails permanently, completed steps may need to be undone. - Progress monitoring — real-time visibility into what's running, what's done, what's blocked.

## What It's For
GPU kernel workflow orchestration with ternary step states. DAG execution, retry on failure, rollback, progress tracking.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 6,064 characters, 173 lines
- Code examples: 5 blocks
- Installation instructions: yes
- Testing mentioned: no
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (5 code blocks)
- Installation/usage instructions provided
- Solid README with good coverage

**Concerns:**
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
