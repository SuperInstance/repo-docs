# field-dynamics-sim

## Intention
**Fleet spectral health simulation — multi-agent field dynamics with cooperative, adversarial, emergent, and phase transition scenarios.**

## How It Works
```
simulation.py     # MultiAgentField: agents, physics, interaction graph
scenarios.py      # 4 predefined scenarios
visualization.py  # Publication-quality matplotlib plots
run_all.py        # Entry point: runs all scenarios
```

## What It's For
- **Cooperative scenario** — all agents share goals, high conservation (CR ≈ 0.95+)
- **Adversarial scenario** — injected rogue agents, conservation drops
- **Emergent scenario** — no cooperation bonus, watch if conservation arises naturally
- **Phase transition** — gradually increase rogue count, detect critical point where fleet coherence collapses
- **Spectral fingerprinting** — effective dimen

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Python

## Status Assessment
Has some documentation (59 lines).

## Honest Assessment
Has documentation (59 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/field-dynamics-sim](https://github.com/SuperInstance/field-dynamics-sim)*
