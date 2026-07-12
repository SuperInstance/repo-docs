# lau-tile-compress

## Intention

Tile compression — store more by storing less. A lossy compression library that preserves meaning, not bytes. Designed for tile-based data (grids, maps, sensor readings) where perfect fidelity is optional but structural integrity matters.

## How It Works

You have tiles — grids of `f64` values — and you want to compress them. This library gives you:
- **Run-Length Encoding (RLE):** Repeated values collapse into (count, value) pairs. Perfect for uniform regions.
- **Delta Encoding:** Store the first value + differences. Ideal for slowly-changing data (heightmaps, temperature grids).
- **Dictionary Encoding:** Repeated patterns of 4 values get mapped to 16-bit codes. First occurrence is literal; subsequent ones are 2 bytes.
- **Threshold Filtering:** Zero out small values based on a quality parameter (0.0 = aggressive, 1.0 = lossless).
- **Semantic Compression:** Group tiles with high cosine similarity and merge them into a single averaged tile.
- **Hybrid:** Automatically picks whichever of RLE or delta produces smaller output.
A `CompressionPipeline` chains multiple stages sequentially, and `CompressionStats` tracks ratios and savings.

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Tile compression — store more by storing less. A lossy compression library that preserves meaning, not bytes. Designed for tile-based data (grids, maps, sensor readings) where perfect fidelity is opti

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (230 lines), mentions tests, includes examples.

- README length: 333 lines, 12163 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (333 lines) with tests, examples, and benchmarks referenced. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
