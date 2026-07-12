# flux-algebra

**Category:** 🎵 Math/Music/Algebra
**Status:** 🟢 Production-oriented
**Language:** Python
**README:** 7,950 bytes

## Intention
Oscar.jl-inspired music algebra — HarmonicRing, PLRGroup, TropicalHarmony, TuningField, DialGeometry. 226 tests.

## How It Works

flux-algebra treats music theory as applied abstract algebra:
- **HarmonicRing**: Z/nZ ring arithmetic for pitch-class theory. Ideals correspond to musical objects (tritone pairs, augmented triads, diminished sevenths, whole-tone scales)
- **PLR Group**: Neo-Riemannian Parallel/Leading-tone/Relative transformations — a group of order 24 acting transitively on 24 major/minor triads
- **Tropical Semiring**: Min-plus algebra applied to voice-leading optimization — avoids cyclic discontinuity of semitone distance
- **Tuning Fields**: Algebraic extensions of Q encoding frequency ratios for equal temperament, just intonation, meantone, microtonal systems
- **Spectral Analysis**: Harmonic graph Laplacian, eigenbasis decomposition, tonality fingerprints

Requires NumPy ≥ 1.24, SciPy ≥ 1.10. Pip-installable. Claims 226 tests.

## What It's For
Computational musicology — applying rigorous abstract algebra (ring theory, group theory, tropical geometry) to music analysis and composition.

## Who Would Use It
Music theorists, computational musicologists, and mathematicians interested in formal approaches to harmony. Also anyone building music analysis software who needs a rigorous algebraic foundation.

## Honest Assessment

**This is the most mathematically substantive repo in the FLUX ecosystem.** The connection between ideals of Z/12Z and recognizable musical objects is legitimate and well-presented. The PLR group is a real concept from neo-Riemannian theory. Tropical semirings for voice-leading optimization is a creative application.

The README is excellent — clear definitions, code examples, mathematical tables, and installation instructions. NumPy/SciPy dependencies are appropriate for the linear algebra required.

**However:** The connection between this music algebra library and a bytecode VM for AI agents is **unclear and possibly nonexistent**. This reads like a standalone computational musicology library that's been prefixed with "flux-" to fit the ecosystem. The Oscar.jl inspiration is legitimate (Oscar is a real computer algebra system), but the "flux" connection feels like branding rather than architecture.

226 tests is a specific, verifiable claim. The mathematical content is real — if you know ring theory, the ideal-as-musical-object mappings check out.

**Bottom line:** Genuinely interesting mathematics, possibly the most intellectually honest repo in the fleet. But its relevance to the FLUX bytecode ecosystem is questionable. This might be better as a standalone library.
