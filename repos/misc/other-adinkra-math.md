# adinkra-math

**Cluster:** math-research  
**Language:** C  
**Source:** [SuperInstance/adinkra-math](https://github.com/SuperInstance/adinkra-math)

## Intention

See README.

## How It Works

> West African Adinkra symbols as mathematics in C — symbolic encoding, topology, supersymmetry, and ML with SVG rendering.

## What It's For

See README.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

C — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (126 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# adinkra-math

> West African Adinkra symbols as mathematics in C — symbolic encoding, topology, supersymmetry, and ML with SVG rendering.

## What This Does

`adinkra-math` is the C implementation of the Adinkra mathematical framework. It provides symbolic encoding of concepts, glyph composition with invariant preservation, topological analysis (Euler characteristic, connected components), supersymmetry Adinkra graphs, concept-space ML (kNN, K-means), and **SVG rendering** of symbols and glyphs. Use it for symbolic AI, educational tools, physics simulations, or generative art.

## The Cultural Root

See `adinkra-math-pypi` (PyPI) for the full cultural background. Adinkra symbols compress complex proverbs into geometric primitives — identical to feature vectors in ML.

## Install

```bash
git clone https://github.com/SuperInstance/adinkra-math.git
cd adinkra-math
make
```

## Quick Start

```c
#include "adinkra_api.h"

int main() {
    char buf[131072];
    Arena arena;
    arena_init(&arena, buf, sizeof(buf));

    // Initialize the system
    AdinkraSystem sys;
    adinkra_system_init(&sys);
    adinkra_system_load_defaults(&sys);

    // Analyze symbols
    adinkra_system_analyze(&sys);

    // Render to SVG
    char *svg = adinkra_system_svg(&sys, 800.0, 600.0);
    printf("%s
", svg);

    // Manual symbol registry
    AdinkraRegistry reg;
    adinkra_registry_init(&arena, &reg, 64);
    adinkra_load_builtin_symbols(&arena, &reg);

    // Concept space and ML
    ConceptSpace cs;
    concept_space_init(&cs, 16);
    int c1 = concept_encode(&cs, "courage", 7, NULL);
    int c2 = concept_encode(&cs, "wisdom", 6, NULL);

    double dist = concept_distance(&cs.concepts[c1], &cs.concepts[c2]);
    printf("Distance: %.3f
", dist);

    // Nearest neighbor
    double query[16] = {0};
    int nearest = concept_nearest(&cs, query, 16);

    // K-means clustering
    ConceptClusters clusters;
    concept_cluster(&cs, &clusters, 2, 50);

    // Topology
    TopoGraph tg;
    topo_graph_init(&tg, 8);
    topo_add_edge(&tg, 0, 1);
    int components = topo_connected_components(&tg);
    int euler = topo_euler_characteristic(&tg);

    arena_destroy(&arena);
    return 0;
}
```

## API Reference

### Symbol Registry (`adinkra.h`)
- `void adinkra_registry_init(Arena *a, AdinkraRegistry *reg, int capacity)`
- `int adinkra_add_symbol(AdinkraRegistry *reg, const char *name, const char *concept, ...)`
- `void adinkra_add_primitive(AdinkraSymbol *sym, PrimitiveType type, ...)`
- `void adinkra_load_builtin_symbols(Arena *a, AdinkraRegistry *reg)`
- `char *adinkra_symbol_to_svg(Arena *a, const AdinkraSymbol *sym, double w, double h)`
- `char *adinkra_registry_to_svg(Arena *a, const AdinkraRegistry *reg, double w, double h)`

### Glyph System (`glyph.h`)
- `void glyph_system_init(GlyphSystem *gs)`
- `int glyph_add(GlyphSystem *gs, const char *name, double semantic_invariant)`
- `int glyph_compose(GlyphSystem *gs, CompositionOp op, int left, int right, double spac
```
