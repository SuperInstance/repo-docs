# fold-compression

## Intention
N-1 evaluations. N! reachable states. The fold sequence IS the compression.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
- GPU fleet: evaluate N-1 SMs, reconstruct all N! orderings
- FPGA: swap operations as 2 multiplexers, 82 swap chains on iCE40
- Distributed fleet: any device fails, reconstruct from generators + parity
- Origami-inspired: Kawasaki conditions = holonomy = RAID parity

## Who Would Use It
```bash
pip install fold-compression
```

## Language / Stack
Python

## Status Assessment
Documented with code examples and API references (61 line README).

## Honest Assessment
Has documentation (61 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/fold-compression](https://github.com/SuperInstance/fold-compression)*
