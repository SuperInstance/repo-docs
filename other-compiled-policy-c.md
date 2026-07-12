# compiled-policy-c

**Cluster:** c-native  
**Language:** C  
**Source:** [SuperInstance/compiled-policy-c](https://github.com/SuperInstance/compiled-policy-c)

## Intention

See README.

## How It Works

### Architecture: Hash → Lookup → Select

[code]

### BLAKE2b-64 State Hashing

Game states are converted to canonical strings (e.g., `"X O X O  "` for tic-tac-toe) and hashed using a compact BLAKE2b-64 implementation (~200 lines of C):

[code]

BLAKE2b is chosen because:

- **Cryptographic strength** — collision resistance prevents state misidentification
- **Compact implementation** — ~200 LOC vs. SHA-256's ~400 LOC
- **Fast on microcontrollers** — ~200 ns per hash on x86, ~2 μs on ESP8266
- **64-bit output** — sufficient for policy tables (< 100K entries), 16 hex chars for human readability

## What It's For

See README.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

C — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (232 lines, 8200 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# compiled-policy-c

**Zero-dependency C library** for deploying compiled tile policies on microcontrollers. Train with gradients in Python, deploy as O(1) hash lookups in C99. Works on ESP8266 (80KB RAM, 4MB flash), Arduino, STM32, and any platform with a C99 compiler.

**Train with gradients, deploy with lookups.**

## Why It Matters

Reinforcement learning produces policies that map game states to actions. In training, this mapping is a neural network — expensive to evaluate, memory-hungry, and requires floating-point hardware. But once training converges, the policy can be **compiled** into a lookup table: hash the state → look up the best action. No floating-point math, no matrix multiplication, no neural network runtime.

This matters enormously for edge deployment:

| Platform | RAM | Flash | Neural Net Feasible? | Lookup Table Feasible? |
|----------|-----|-------|---------------------|----------------------|
| ESP8266 | 80 KB | 4 MB | ❌ (no FPU, ~50KB free) | ✅ (< 5 KB) |
| Arduino Uno | 2 KB | 32 KB | ❌ | ✅ (< 1 KB for small policy) |
| STM32F103 | 20 KB | 128 KB | ❌ (no FPU on Cortex-M0) | ✅ (< 10 KB) |
| Raspberry Pi Zero | 512 MB | 16 GB | ✅ (slowly) | ✅ |

The compiled-policy approach has three advantages over on-device inference:

1. **Deterministic latency** — O(1) hash lookup completes in <300 ns regardless of policy complexity
2. **Zero dependencies** — only `string.h`, `stdint.h`, `stdlib.h` (C99 standard library)
3. **Provably correct** — the lookup table IS the policy; no inference bugs, no floating-point drift

## How It Works

### Architecture: Hash → Lookup → Select

```
Game State (string)
       │
       ▼
  BLAKE2b-64 ──► 16 hex chars
       │
       ▼
  Hash Table (FNV-1a buckets)
       │
       ▼
  Policy Entry {hash, action, score}
       │
       ▼
  Softmax Selection (optional, temperature-controlled)
       │
       ▼
  Best Action
```

### BLAKE2b-64 State Hashing

Game states are converted to canonical strings (e.g., `"X O X O  "` for tic-tac-toe) and hashed using a compact BLAKE2b-64 implementation (~200 lines of C):

```
hash = BLAKE2b-64(state_string)
output: 16 hex chars (8 bytes → 16 hex nibbles)
```

BLAKE2b is chosen because:

- **Cryptographic strength** — collision resistance prevents state misidentification
- **Compact implementation** — ~200 LOC vs. SHA-256's ~400 LOC
- **Fast on microcontrollers** — ~200 ns per hash on x86, ~2 μs on ESP8266
- **64-bit output** — sufficient for policy tables (< 100K entries), 16 hex chars for human readability

**Complexity:** BLAKE2b hashing is O(N) where N = input length. For typical game states (< 64 chars), this is effectively O(1).

### FNV-1a Hash Table

The 16-char hex hash is mapped to a table bucket using **FNV-1a** (Fowler-Noll-Vo):

```
bucket = FNV-1a(hash_string) mod TABLE_SIZE
```

The hash table uses **separate chaining** (linked list per bucket) with TABLE_SIZE = 256:

```
bucket[i] → entry → entry → entry → NULL
```

**Load factor:** α = N / TABLE_SI
```
