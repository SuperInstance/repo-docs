# flux-hardware

**Category:** ⚡ Hardware/GPU
**Status:** 🟢 Production-oriented
**Language:** C
**README:** 11,582 bytes

## Intention
FLUX hardware backends: CUDA, AVX-512, Fortran, FPGA, eBPF, WebGPU, Vulkan, Coq. Three-tier constraint enforcement.

## How It Works

A cross-platform framework for high-throughput constraint checking, targeting every major hardware backend:
- **CUDA**: 5 specialized GPU kernels (basic, warp-vote, shared-cache, tensor core, mixed-precision)
- **AVX-512**: Vectorized x86_64 CPU operations with JIT-compiled kernel variants
- **FPGA**: Synthesizable Verilog RTL (`flux_checker_top.sv`, 1,717 LUTs on Xilinx Artix-7)
- **WebGPU**: WGSL compute shaders for browser-based checking
- **Vulkan**: SPIR-V compute shaders for cross-vendor GPU support
- **eBPF**: XDP network firewall filters for kernel-level enforcement
- **Fortran**: OpenMP parallel reference implementation

Claims 210 formal test cases + 5.58M randomized trials with zero differential mismatches. Peak throughput: 70.1B checks/s on 12-thread Xeon Scalable, 1.02B checks/s on RTX 4050.

## What It's For
Hardware-accelerated constraint checking across every compute platform — from browser to data center to embedded FPGA.

## Who Would Use It
HPC engineers, embedded systems developers, and anyone needing high-throughput constraint validation on specific hardware. The Safe-TOPS/W metric targets safety-certified environments.

## Honest Assessment

**The most ambitious repo in the ecosystem** — targeting 8+ hardware backends with formal verification claims. The README is detailed (11.6KB) with extensive benchmark tables, architecture diagrams, and per-backend optimization details.

**The benchmark numbers are the key claims to scrutinize:**
- 70.1B checks/s on 12-thread Xeon — this is plausible for simple bitwise checks (the constraint operations ARE simple: range checks, domain checks, mask comparisons). For context, simple operations on modern CPUs can hit hundreds of billions of ops/s with SIMD.
- 1.02B checks/s on RTX 4050 — plausible for a GPU kernel doing simple comparisons
- 24.9B checks/s on RTX 4050 (claimed in flux-gpu) — **wait, these two repos claim different numbers for similar hardware.** Inconsistency worth investigating.

**Red flags:**
- "Zero-Defect Guarantee" from 5.58M randomized trials is not a guarantee — it's evidence. Real formal verification (Coq proofs) is mentioned but not shown in detail.
- The Safe-TOPS/W metric (410M CPU / 241M GPU) is a custom metric — its usefulness and methodology aren't clearly defined.
- "Production-grade" is a strong claim for a repo in an ecosystem full of experimental/stub repos.
- Targeting FPGA, eBPF, WebGPU, Vulkan, CUDA, AVX-512, and Fortran simultaneously requires enormous engineering effort — is this all actually implemented, or are some backends aspirational?

**Bottom line:** If real, this is a serious engineering achievement. The scope (8 hardware targets with formal verification) would require a team of specialists. The benchmark claims are in the right ballpark for simple operations. But the gap between the claims and what can be independently verified is significant. Proceed with cautious interest.
