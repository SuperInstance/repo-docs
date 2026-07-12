# limits-colimits

## Intention

Category theory limits and colimits: concrete implementations for Set with products, coproducts, pullbacks, pushouts, equalizers, and coequalizers

## How It Works

### Why Concrete Types?
Many category theory libraries in Rust use type-level programming (associated types, generic lifetimes, trait objects) to abstract over categories. This is powerful but opaque.
This crate makes a deliberate choice: **work exclusively in the category Set**, using `Vec<String>` for sets and `HashMap<String, String>` for morphisms. This makes every construction inspectable, printable, and debuggable. You can see exactly what a product, pullback, or coequalizer looks like as data.
### Why String-Based?
Using `String` elements means:
- No generic type parameters cluttering signatures
- Easy to print and inspect results
- Morphisms can be serialized with `serde`
- The focus stays on the categorical structure, not Rust's type system
### Morphisms as HashMaps
A morphism $f: A \to B$ in Set is literally a function — a mapping from elements of $A$ to elements of $B$. Using `HashMap<String, String>` is the most direct representation. Partial morphisms (some elements unmapped) are supported; total morphisms map every domain element.
### Universal Property Verification
Every construction provides a method to verify the universal property:
- `ProductMorphism::verify_universal_property()` checks $\pi_i \circ \langle f_1, \ldots, f_n \rangle = f_i$
- `CoproductMorphism::verify_universal_property()` checks $[f_1, \ldots, f_n] \circ \iota_i = f_i$

## What It's For

Category theory limits and colimits: concrete implementations for Set with products, coproducts, pullbacks, pushouts, equalizers, and coequalizers

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (380 lines), includes examples.

- README length: 524 lines, 17823 characters
- Documented sections: Table of Contents, Motivation, Theory, Modules, Design Decisions

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (524 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
