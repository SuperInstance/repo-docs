# ExocortexTDA.jl

## Intention
Topological data analysis for the exocortex — proving multiple dispatch makes TDA readable and composable.

## How It Works
```
  ┌─────────────┐
  │  Point Cloud │  ── or any metric space
  └──────┬──────┘
         │  VietorisRipsFiltration()
         ▼
  ┌─────────────┐
  │  Filtration  │  sorted simplices + values
  └──────┬──────┘
         │  boundary_matrix()
         ▼
  ┌─────────────┐
  │   Boundary   │  mod-2 sparse matrix
  │    Matrix    │
  └──────┬──────┘
         │  reduce_matrix!()
         ▼
  ┌─────────────┐
  │  Persistence │  (birth, death) pairs
  │   Barcode    │
  └──┬───┬───┬──┘
     │   │   │

## What It's For
> *Multiple dispatch makes the topology match the mathematics.*

In TDA, the same operation has different meanings depending on context. Computing Betti numbers from a barcode, a simplicial complex, or a filtration are conceptually identical but algorithmically distinct. Julia's multiple dispatch lets you write `betti_numbers(x)` and get the right implementation automatically — no visitor patterns

## Who Would Use It
```julia

## Language / Stack
Julia

## Status Assessment
Documented with code examples and API references (577 line README).

## Honest Assessment
Well-documented (577 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/ExocortexTDA.jl](https://github.com/SuperInstance/ExocortexTDA.jl)*
