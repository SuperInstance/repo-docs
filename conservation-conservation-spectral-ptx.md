# conservation-spectral-ptx

## Summary
PTX-native GPU kernels.

## Intention
Port the Conservation Spectral SDK to ptx, demonstrating spectral graph analysis in any language while revealing paradigm-specific insights.

## How It Works
Implements the same pipeline: build tension graph, construct Laplacian (L = D - A), eigendecomposition, compute conservation ratio CR = lambda_2/lambda_n, detect anomalies. Each language highlights different paradigm strengths.

## What It's For
- Spectral graph analysis in ptx

## Who Would Use It
- Developers working in ptx
- Researchers comparing language paradigms for spectral computation

## Language/Stack
- **Primary language:** Cuda

## Status Assessment
**No README available.**

## Honest Assessment
The ptx port is well-crafted with language-specific insights. Idiomatic implementation. The polyglot SDK is impressive as a whole, but each port has limited standalone value.
