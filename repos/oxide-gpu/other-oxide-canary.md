# oxide-canary

## Intention
Canary deployments for GPU kernel versions with ternary health verdict. Progressive rollout, automatic rollback, metric comparison.

## How It Works
Progressive, self-healing canary deployments for GPU kernel versions. Deploying a new GPU kernel is a high-stakes operation. A single regression in a CUDA or ROCm kernel can bring down an inference pipeline, corrupt training checkpoints, or silently degrade model accuracy for hours before anyone notices. Traditional blue-green deployments work well for stateless web services, but they fall short when the unit of deployment is a compiled kernel whose behavior can only be validated under real-world load and hardware conditions. Canary releases solve this by exposing the new kernel to a small, controlled slice of production traffic and observing how it behaves in situ. If metrics hold steady, you gradually increase traffic. If something goes wrong, you roll back before most users are affected

## What It's For
Canary deployments for GPU kernel versions with ternary health verdict. Progressive rollout, automatic rollback, metric comparison.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 8,065 characters, 174 lines
- Code examples: 8 blocks
- Installation instructions: yes
- Testing mentioned: yes
- License mentioned: yes
- API documentation: no
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (8 code blocks)
- Installation/usage instructions provided
- Testing mentioned
- Solid README with good coverage

**Concerns:**
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
