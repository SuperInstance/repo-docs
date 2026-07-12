# oxide-loadshed

## Intention
Load shedding for GPU job queues with ternary admission. Priority-based shedding, coordinated backoff, graceful recovery.

## How It Works
Load shedding for GPU job queues with ternary admission control and coordinated backoff. When GPU capacity runs out, you have three choices: accept the job and risk OOM/crash (bad), silently drop it (worse), or explicitly tell the submitter why it was rejected (correct). Load shedding is the disciplined version of that third option. Every incoming job gets a ternary admission decision: Admit (+1, capacity available), Queue (0, approaching limits but not critical), or Shed (-1, over capacity, reject). The system goes further than simple rejection. It sends backoff signals to upstream producers (Normal / SlowDown / Stop), sheds lowest-priority jobs first when forced, and gradually recovers admission thresholds as the queue drains. This means the system degrades gracefully under load instead 

## What It's For
Load shedding for GPU job queues with ternary admission. Priority-based shedding, coordinated backoff, graceful recovery.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 7,822 characters, 174 lines
- Code examples: 6 blocks
- Installation instructions: no
- Testing mentioned: no
- License mentioned: no
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (6 code blocks)
- Solid README with good coverage

**Concerns:**
- No clear installation instructions
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
