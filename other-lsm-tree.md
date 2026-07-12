# lsm-tree

## Intention

Research-grade Rust crate

## How It Works

```rust
use lsm_tree::LsmTree;
let mut tree = LsmTree::new(100); // memtable capacity 100
tree.put(b"key", b"value");
assert_eq!(tree.get(b"key"), Some(b"value".to_vec()));
```

## What It's For

Research-grade Rust crate

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: LIGHT**

Short README (22 lines), includes examples.

- README length: 30 lines, 763 characters
- Documented sections: Features, Usage, Modules

## Honest Assessment

Some documentation exists but it's not comprehensive. The project may have working code, but the README doesn't provide enough evidence of maturity, testing, or real-world use. **Promising direction, needs more evidence of substance.**
