# flux-gpu

**Category:** ⚡ Hardware/GPU
**Status:** 🟡 Development
**Language:** Cuda
**README:** 3,750 bytes

## Intention
CUDA micro-experiments for constraint engine — 24.9B checks/sec on RTX 4050. Sediment, BFS, hyperbolic on GPU.

## How It Works
The error mask (1 byte per value, 1 bit per constraint) maps perfectly to GPU execution: each thread reads one value, checks it against all constraints, writes one byte. No warp divergence. No scattered writes. No synchronization needed between threads.

The constraint bounds fit in shared memory (8 doubles = 64 bytes). Each thread block loads them once, then processes thousands of values through the same tight loop.

## Kernels

### `exact_check_kernel.cu` — The Core

Each thread checks one val...

## What It's For
CUDA micro-experiments for constraint engine — 24.9B checks/sec on RTX 4050. Sediment, BFS, hyperbolic on GPU.

## Who Would Use It
Systems engineers and HPC developers targeting specific hardware (NVIDIA GPUs, FPGAs, AVX-512 CPUs).

## Honest Assessment
Has code examples. missing: tests, CI. Has implementation code but **test coverage needs verification**.. GPU acceleration claim — verify with actual hardware benchmarks..
