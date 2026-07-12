# entropy-lint

## Intention
**Information entropy analysis for code quality.**

## How It Works
```
composite = token_entropy × 0.40 + function_entropy × 0.25 + name_entropy × 0.25 + test_entropy × 0.10
```

## What It's For
| Metric | Module | What It Means |
|--------|--------|---------------|
| Token entropy | `TokenEntropy` | Shannon entropy of token distribution — high = diverse vocabulary = doing too many things |
| Function entropy | `FunctionEntropy` | Entropy of function length distribution — high = mixed abstraction levels (tiny + huge functions) |
| Name entropy | `NameEntropy` | Normalized character entrop

## Who Would Use It
```bash
cargo install --path .
```

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (152 line README).

## Honest Assessment
Moderately documented (152 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/entropy-lint](https://github.com/SuperInstance/entropy-lint)*
