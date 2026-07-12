# exocortex-ast-cpp

## Intention
A C++17 header-only AST decomposition engine for parsing C/C++/Rust-like source code into structured nodes and extracting dependency graphs.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
- **ASTNode**: Represents source constructs with kind, name, source range, and children
- **ASTDecomposer**: Recursive-descent tokenizer + parser (no external dependencies)
- **DependencyGraph**: Extracts call references between functions
- Parses: function declarations, struct/class definitions, namespace blocks
- Header-only: just `#include "exocortex_ast.hpp"`

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
C++

## Status Assessment
Documented with code examples and API references (53 line README).

## Honest Assessment
Has documentation (53 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/exocortex-ast-cpp](https://github.com/SuperInstance/exocortex-ast-cpp)*
