# grand-pattern-embedded

## Intention
Grand Pattern for microcontrollers — `no_std`, fixed memory, ESP32/Arduino/ARM Cortex-M.

## How It Works
```
Room ─── Vibe (f64) ─── JEPA (predictor)
  │
  ├── CellGraph (32 rooms, 64 edges, diffusion)
  │
  └── Murmur (32-byte gossip message)
       │
       └── Transport (Wi-Fi / BLE / UART / I2C)
```

## What It's For
- **`no_std` compatible** — zero heap allocation, fixed-size arrays everywhere
- **JEPA predictor** — sliding window prediction with learned weights (max 16 readings)
- **CellGraph** — up to 32 rooms, 64 edges, diffusion-based vibe propagation
- **Murmur gossip** — 32-byte fixed messages, serializable for any transport
- **Transport stubs** — Wi-Fi, BLE, UART, I2C (compile for any target, implemen

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (72 line README).

## Honest Assessment
Has documentation (72 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/grand-pattern-embedded](https://github.com/SuperInstance/grand-pattern-embedded)*
