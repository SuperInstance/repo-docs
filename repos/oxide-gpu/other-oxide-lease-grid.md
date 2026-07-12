# oxide-lease-grid

## Intention
Grid-based lease matrix for multi-GPU allocation with ternary cells. 2D block allocation, fragmentation metrics, compaction.

## How It Works
Grid-based lease matrix for multi-GPU spatial resource allocation. GPU resources aren't just scalar quantities you can divide with percentages. On a multi-GPU system, allocation is spatial: which GPU, which memory region, which compute unit. A "lease" is a claim on a specific cell in a resource grid. The grid models the spatial nature of GPU allocation — you can't lease the same SM to two kernels simultaneously, and you need contiguous blocks for some operations. The ternary cell model captures the lifecycle: Free (-1, available), Reserved (0, claimed but not active), Leased (+1, actively in use). This three-state model handles the common pattern where a kernel reserves resources during compilation but doesn't activate them until dispatch. It also prevents double-allocation without locks —

## What It's For
Grid-based lease matrix for multi-GPU allocation with ternary cells. 2D block allocation, fragmentation metrics, compaction.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 5,520 characters, 120 lines
- Code examples: 3 blocks
- Installation instructions: no
- Testing mentioned: no
- License mentioned: no
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (3 code blocks)
- Solid README with good coverage

**Concerns:**
- No clear installation instructions
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
