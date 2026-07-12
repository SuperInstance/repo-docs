# async-gpu-dispatch

**Cluster:** gpu-native-compute  
**Language:** Rust  
**Source:** [SuperInstance/async-gpu-dispatch](https://github.com/SuperInstance/async-gpu-dispatch)

## Intention

Experiment: async GPU kernel dispatch modeled on open-parallel's tokio-style runtime. Tests how futures, channels, and task scheduling compose with GPU command queues.

## How It Works

### Command Model

Each `GpuCommand` carries:

| Field | Type | Description |
|-------|------|-------------|
| `kernel_name` | String | Kernel identifier (e.g., "matmul", "attention") |
| `block_dim` | (u32, u32, u32) | CUDA-style block dimensions |
| `shared_mem` | u32 | Shared memory per block (bytes) |
| `priority` | CommandPriority | Low, Normal, High, Critical |
| `submitted_at` | Instant | Timestamp for latency measurement |

### Priority Scheduling

The `execute_by_priority()` method performs a **linear scan** to find the highest-priority pending command. This is O(n) per dispatch — acc

## What It's For

Experiment: async GPU kernel dispatch modeled on open-parallel's tokio-style runtime. Tests how futures, channels, and task scheduling compose with GPU command queues.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (136 lines, 5949 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# async-gpu-dispatch

**Async GPU kernel dispatch modeled on tokio-style runtime semantics — futures, priority queues, and pipeline composition for GPU command buffers.**

GPU programming models are fundamentally asynchronous: kernels are submitted to command queues, execute on the device, and return results via polling or callbacks. `async-gpu-dispatch` models this interaction using patterns from async Rust runtimes (tokio, async-std): `submit()` is non-blocking (like `tokio::spawn`), `poll()` checks for completion (like `Future::poll`), and priority dispatch mirrors tokio's work-stealing scheduler.

## Why It Matters

Modern ML and HPC workloads submit thousands of GPU kernels per second. The dispatch layer — how commands are queued, prioritized, and scheduled — directly impacts throughput and latency. Key challenges:

- **Queue depth management**: Too shallow → GPU starves. Too deep → latency spikes.
- **Priority inversion**: Low-priority kernels blocking the pipeline.
- **Pipeline composition**: Chaining kernels (filter → transform → reduce) requires ordered dispatch with data dependencies.
- **Backpressure**: When the queue is full, callers need clear feedback (`QueueFull` error) to implement adaptive submission rates.

This crate provides a clean simulation of these dynamics, useful for:

- **Benchmarking dispatch strategies** before deploying on real hardware
- **Teaching async runtime concepts** with a concrete, visual domain (GPU kernels)
- **Prototyping priority scheduling algorithms** without CUDA/Vulkan boilerplate

## How It Works

### Command Model

Each `GpuCommand` carries:

| Field | Type | Description |
|-------|------|-------------|
| `kernel_name` | String | Kernel identifier (e.g., "matmul", "attention") |
| `block_dim` | (u32, u32, u32) | CUDA-style block dimensions |
| `shared_mem` | u32 | Shared memory per block (bytes) |
| `priority` | CommandPriority | Low, Normal, High, Critical |
| `submitted_at` | Instant | Timestamp for latency measurement |

### Priority Scheduling

The `execute_by_priority()` method performs a **linear scan** to find the highest-priority pending command. This is O(n) per dispatch — acceptable for simulation but real GPUs use hardware priority queues.

Priority ordering: Critical (3) > High (2) > Normal (1) > Low (0). Among equal priorities, FIFO order is preserved (stable selection).

### Simulated Execution Times

| Priority | Simulated Execution (μs) | Throughput (ops/s) |
|----------|-------------------------|---------------------|
| Critical | 50 | 20,000 |
| High | 100 | 10,000 |
| Normal | 200 | 5,000 |
| Low | 500 | 2,000 |

### Pipeline Composition

`submit_pipeline(&["filter", "transform", "reduce"])` chains kernels with decreasing priority (first kernel = High, rest = Normal). This models a **dataflow pipeline** where each stage's output feeds the next:

```
filter(High) → transform(Normal) → reduce(Normal)
```

### Task Abstraction

`GpuTask` wraps a command with lifecycle state: Pending
```
