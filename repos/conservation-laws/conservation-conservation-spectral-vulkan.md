# conservation-spectral-vulkan

## Summary
Vulkan compute shaders.

## Intention
Port the Conservation Spectral SDK to vulkan, demonstrating spectral graph analysis in any language while revealing paradigm-specific insights.

## How It Works
Implements the same pipeline: build tension graph, construct Laplacian (L = D - A), eigendecomposition, compute conservation ratio CR = lambda_2/lambda_n, detect anomalies. Each language highlights different paradigm strengths.

## What It's For
- Spectral graph analysis in vulkan

## Who Would Use It
- Developers working in vulkan
- Researchers comparing language paradigms for spectral computation

## Language/Stack
- **Primary language:** C++

## Status Assessment
**No README available.**

## Honest Assessment
The vulkan port is well-crafted with language-specific insights. Idiomatic implementation. The polyglot SDK is impressive as a whole, but each port has limited standalone value.
