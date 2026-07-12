# cudaclaw

**Cluster:** gpu-native-compute  
**Language:** Rust  
**Source:** [SuperInstance/cudaclaw](https://github.com/SuperInstance/cudaclaw)

## Intention

⚡ GPU-accelerated SmartCRDT with persistent CUDA kernels — warp-level consensus.

## How It Works

**Unified Memory Architecture:**
The command queue is allocated in CUDA Unified Memory via `cust::memory::UnifiedBuffer`. Both CPU and GPU access the same physical memory page — the CUDA driver handles migration and coherence automatically. This enables zero-copy communication:

[code]

**Lock-free queue:**
Head and tail indices use atomic operations (`atomicAdd`, `atomicCAS`) for thread-safe concurrent access. The queue is bounded (ring buffer), preventing unbounded memory growth.

**Persistent worker kernel:**
Unlike the traditional launch-process-terminate cycle, CudaClaw's kernel stays ali

## What It's For

⚡ GPU-accelerated SmartCRDT with persistent CUDA kernels — warp-level consensus.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (89 lines, 4361 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# CudaClaw

**CudaClaw** is a Rust + CUDA library implementing a GPU-resident persistent worker kernel for agent command dispatch — featuring lock-free command queues in unified memory, sub-microsecond host-device communication, and warp-level parallelism for the SuperInstance agent fleet.

## Why It Matters

GPU computing for AI agents has traditionally focused on neural network inference (cuDNN, TensorRT). CudaClaw takes a fundamentally different approach: it runs the *agent dispatch loop itself* on the GPU, treating the GPU as a general-purpose parallel agent processor. A persistent CUDA kernel stays resident on the GPU, polling a lock-free command queue in unified memory. This eliminates the kernel-launch overhead (typically 5–20 μs per launch) that dominates latency in traditional host-driven GPU workflows. The result: command dispatch at sub-microsecond latency, with warp-level parallelism enabling 32 agents to be serviced simultaneously per warp scheduler. For fleet-scale simulations with thousands of agents, this represents a 10–100× throughput improvement over CPU-based dispatch.

## How It Works

**Unified Memory Architecture:**
The command queue is allocated in CUDA Unified Memory via `cust::memory::UnifiedBuffer`. Both CPU and GPU access the same physical memory page — the CUDA driver handles migration and coherence automatically. This enables zero-copy communication:

```
// CPU writes command
queue.commands[0] = Command { op: Add, a: 1.0, b: 2.0 };
queue.status = STATUS_READY;

// GPU polls (persistent kernel)
while (queue->status != STATUS_READY) { __nanosleep(100); }
result = queue->commands[0].a + queue->commands[0].b;
queue->status = STATUS_DONE;
```

**Lock-free queue:**
Head and tail indices use atomic operations (`atomicAdd`, `atomicCAS`) for thread-safe concurrent access. The queue is bounded (ring buffer), preventing unbounded memory growth.

**Persistent worker kernel:**
Unlike the traditional launch-process-terminate cycle, CudaClaw's kernel stays alive indefinitely:

```
__global__ void persistent_worker(CommandQueue* queue) {
    while (true) {
        // Warp-level poll for commands
        if (queue->has_pending()) {
            process_command(queue->dequeue());
        }
        __nanosleep(100); // yield
    }
}
```

**Memory alignment:** All structs use `#[repr(C)]` with explicit alignment matching the CUDA-side definitions. `Command` is 48 bytes, 32-byte aligned. `CommandQueue` is 896 bytes, 128-byte aligned. Compile-time assertions verify layout consistency.

**Performance metrics:**
- Command dispatch latency: < 1 μs (unified memory path)
- Kernel launch overhead: eliminated (persistent kernel)
- Warp utilization: measured via consecutive idle vs. busy cycles

## Quick Start

```rust
// Requires CUDA toolkit and `cuda` feature enabled
// cargo run --features cuda

use cuda_claw::{CommandQueueHost, Command, CommandType};

fn main() {
    let queue = CommandQueueHost::default();
    let cmd = Command::new(Command
```
