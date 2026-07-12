# flux-chapel

**Category:** 🏛️ Legacy/Niche Language Port
**Status:** 🟡 Development
**Language:** Chapel
**README:** 3,052 bytes

## Intention
Chapel constraint engine with GPU locale model. Multi-GPU coforall, distributed checking.

## How It Works
Chapel's `locale` model treats every compute target — CPU cores, GPUs, remote nodes — as a locale. You don't write GPU code. You write code that runs *on a locale*, and Chapel handles the rest.

```chapel
on here.gpus[0] {
    // This block runs on GPU 0
    forall i in 0..#n {
        masks[i] = checkValue(values[i], constraints);
    }
}
```

For constraint checking, this means the same code works on CPU, GPU, or distributed clusters. The locality is explicit. The parallelism is implicit.

## ...

## What It's For
Chapel constraint engine with GPU locale model. Multi-GPU coforall, distributed checking.

## Who Would Use It
Systems engineers and HPC developers targeting specific hardware (NVIDIA GPUs, FPGAs, AVX-512 CPUs).

## Honest Assessment
Has code examples. missing: tests. Has implementation code but **test coverage needs verification**..
