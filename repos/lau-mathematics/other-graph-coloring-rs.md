# graph-coloring-rs

## Intention
**Graph coloring algorithms in pure Rust.**

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
```
Need a valid coloring fast?
└── Greedy (always works, might use extra colors)

Need a good coloring?
├── Graph has many high-degree vertices? → Welsh-Powell
└── General case? → DSATUR (best heuristic)

Need the EXACT minimum?
└── Small graph (V ≤ 20)? → chromatic_number_exact
└── Large graph? → Use lower/upper bounds to bracket it
```

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (249 line README).

## Honest Assessment
Well-documented (249 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/graph-coloring-rs](https://github.com/SuperInstance/graph-coloring-rs)*
