# flux-algebra-c

**Category:** 🎵 Math/Music/Algebra
**Status:** 🟢 Production-oriented
**Language:** C
**README:** 6,629 bytes

## Intention
C port of flux-algebra — PLR group, tuning fields, voice leading

## How It Works
```c
#include "flux_algebra.h"

<<<<<<< HEAD
Chord cmaj = chord_major(0);          /* C major */
Chord amin = relative(&cmaj);         /* A minor (relative) */
Chord bmin = leading_tone(&cmaj);     /* B diminished (leading tone) */
Chord cmin = parallel(&cmaj);         /* C minor (parallel) */

/* Tuning systems */
TuningField ji = tuning_just_intonation();
double freq = tuning_frequency(&ji, 64);   /* E4 in just intonation */
double cents = tuning_cents_deviation(&ji, 64);

/* Tropical semiring...

## What It's For
C port of flux-algebra — PLR group, tuning fields, voice leading

## Who Would Use It
Researchers and developers at the intersection of music theory, abstract algebra, and computation. Niche academic/experimental audience.

## Honest Assessment
Has real code examples and installation instructions. claims 11 tests. missing: benchmarks. Mathematically sophisticated concept (music-as-algebra) — interesting research angle but niche..
