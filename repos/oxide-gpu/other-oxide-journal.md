# oxide-journal

## Intention
Write-ahead journal for GPU state mutations with ternary integrity. Replay, verify, checkpoint, compaction.

## How It Works
Write-ahead journal for GPU state mutations with ternary integrity. GPU kernels mutate state: memory buffers, tensor shapes, execution contexts. When a kernel crashes mid-execution or a node dies, you need to know exactly what state was durable and what was in-flight. Database people solved this decades ago with write-ahead logs. This is the same idea, adapted for GPU compute. The ternary integrity model is the key innovation. Every journal entry is one of three states: Committed (+1, durable and verified), Pending (0, written but not yet confirmed), or Corrupted (-1, checksum mismatch). After a crash, you replay committed entries, discard pending ones, and flag corrupted ones. No ambiguity, no heuristic recovery.

## What It's For
Write-ahead journal for GPU state mutations with ternary integrity. Replay, verify, checkpoint, compaction.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 5,317 characters, 123 lines
- Code examples: 4 blocks
- Installation instructions: no
- Testing mentioned: yes
- License mentioned: no
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (4 code blocks)
- Testing mentioned
- Solid README with good coverage

**Concerns:**
- No clear installation instructions
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
