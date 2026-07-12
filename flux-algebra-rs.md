# flux-algebra-rs

**Category:** 🎵 Math/Music/Algebra
**Status:** 🟡 Development
**Language:** Rust
**README:** 5,638 bytes

## Intention
Musical algebra — PLR group, tropical semiring, tuning fields, voice leading

## How It Works
```rust
use flux_algebra::{HarmonicRing, PlrGroup, Triad, TropicalSemiring, TuningField};

// Pitch-class ring ℤ/12ℤ: a perfect fifth + a perfect fourth = an octave.
let ring = HarmonicRing::chromatic();
assert_eq!(ring.add(7, 5), 0);          // 7 + 5 ≡ 0 (mod 12)
assert_eq!(ring.transpose(&[0u32, 4, 7], 5), vec![5, 9, 0]); // C major → F major

// Neo-Riemannian transformations.
let c_major = Triad::major(0);
let c_minor = PlrGroup::p(c_major);     // Parallel: Cm
let e_minor = PlrGroup::l(Tri...

## What It's For
Musical algebra — PLR group, tropical semiring, tuning fields, voice leading

## Who Would Use It
Researchers and developers at the intersection of music theory, abstract algebra, and computation. Niche academic/experimental audience.

## Honest Assessment
Has real code examples and installation instructions. missing: benchmarks. Mathematically sophisticated concept (music-as-algebra) — interesting research angle but niche..
