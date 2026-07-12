# consensus

**Cluster:** cs-implementations  
**Language:** HTML  
**Source:** [SuperInstance/consensus](https://github.com/SuperInstance/consensus)

## Intention

Zero-holonomy consensus Python wrapper, P48 validator, tile cardinality tracker

## How It Works

[code]

### Core Components

| File | Purpose |
|------|---------|
| `holonomy.py` | Python wrapper + pure Python fallback |
| `tile_cardinality_tracker.py` | Constraint drift detection across PLATO rooms |
| `dashboard/index.html` | Browser-based fleet consensus visualizer |

### Formalisms

The consensus engine tracks three constraint formalisms:

- **Laman** — rigidity theory, `beta_1 = V - 2` (planar graphs)
- **H1** — first cohomology, cycle space emergence
- **P48** — 48-direction trust lattice, U(24,24) half-plane decomposition

P48 is a **post-snap validator** — it runs after matroid u

## What It's For

Zero-holonomy consensus Python wrapper, P48 validator, tile cardinality tracker

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

HTML — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (272 lines, 7797 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# Zero-Holonomy Consensus

**Consensus engine for PLATO-powered agent fleets.** Validates that a network of tiles forms a globally consistent constraint system via zero-holonomy checks.

```
pip install consensus          # coming soon
git clone https://github.com/SuperInstance/consensus.git
cd consensus && python holonomy.py --tiles 50
```

---

## What Is Zero-Holonomy Consensus?

Imagine walking around a closed loop in a network of tiles, composing the rotations you encounter at each step. If you end up facing the same direction you started — **identity holonomy** — every cycle is locally consistent, and the whole network is globally sound.

**Zero-holonomy consensus** applies this idea to constraint systems:
- Each tile carries a **holonomy matrix** (3×3 rotation)
- Each edge composes neighboring tile constraints
- Each cycle composed around the network must return ≈ identity
- Deviation from identity = constraint drift = inconsistent state

This is the same math behind parallel transport in curved spaces, but applied to agent fleet topology.

---

## Quick Start

```bash
# Clone
git clone https://github.com/SuperInstance/consensus.git
cd consensus

# Run a quick consensus check (50 simulated tiles)
python holonomy.py --tiles 50

# JSON output for scripting
python holonomy.py --tiles 20 --json
```

**Output:**
```
Zero-Holonomy Check: 50 tiles
  ✅ CONSISTENT
  Deviation: 0.000042
  Info content: 0.0312 bits
```

---

## Python API

```python
from holonomy import (
    HolonomyMatrix,   # 3x3 rotation matrix
    ConsensusTile,    # tile with holonomy + neighbors
    check_consensus,  # O(C·L) zero-holonomy check
    quick_check,      # simulate a fleet
)

# Build a network of tiles
tiles = [
    ConsensusTile(
        id=0,
        holonomy=HolonomyMatrix.from_axis_angle([0, 0, 1], 0.01),
        neighbors=[1, 2],
    ),
    ConsensusTile(
        id=1,
        holonomy=HolonomyMatrix.from_axis_angle([0, 1, 0], 0.02),
        neighbors=[0, 2],
    ),
    ConsensusTile(
        id=2,
        holonomy=HolonomyMatrix.from_axis_angle([1, 0, 0], 0.015),
        neighbors=[0, 1],
    ),
]

# Check consensus — all cycles must return identity
result = check_consensus(tiles)

print(f"Consistent: {result.is_consistent}")
print(f"Deviation:  {result.deviation:.6f}")
print(f"Faulty tile: {result.faulty_tile}")  # None if consistent
print(f"Information: {result.information:.4f} bits")
```

### HolonomyMatrix

```python
# Identity matrix
H = HolonomyMatrix.identity()

# From axis-angle rotation (Rodrigues' formula)
H = HolonomyMatrix.from_axis_angle([0, 0, 1], 0.1)

# Compose two holonomies
H_combined = H1.multiply(H2)

# Check if close to identity
H.is_identity(tolerance=1e-6)  # True/False

# Deviation from identity (norm of M - I)
dev = H.deviation()

# Serialize to 72 bytes
b = H.to_bytes()

# Deserialize
H2 = HolonomyMatrix.from_bytes(b)
```

### ConsensusTile

```python
@dataclass
class ConsensusTile:
    id: int                    # unique tile ID
  
```
