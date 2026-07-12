# oxide-tenancy

## Intention
Multi-tenant GPU isolation with ternary quality signals. Fair-share scheduling, interference detection, quarantine, rebalancing.

## How It Works
Multi-tenant GPU isolation with ternary quality signals. When multiple tenants share a GPU — different teams, different workloads, different SLAs — you can't just hand out time slices and hope for the best. GPUs have shared memory bandwidth, shared L2 cache, shared SM schedulers. One tenant's memory-hungry kernel can degrade another's latency by 40% without either exceeding its nominal allocation. The core insight: isolation quality is not binary. A tenant can be fully isolated (+1), cooperatively sharing (0), or actively interfering (-1). This ternary signal drives every decision — allocation, quarantine, rebalancing — without needing exact interference measurements (which are expensive and often unavailable on real hardware).

## What It's For
Multi-tenant GPU isolation with ternary quality signals. Fair-share scheduling, interference detection, quarantine, rebalancing.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 5,770 characters, 124 lines
- Code examples: 4 blocks
- Installation instructions: no
- Testing mentioned: no
- License mentioned: no
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (4 code blocks)
- Solid README with good coverage

**Concerns:**
- No clear installation instructions
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
