# aho-corasick-rs

**Cluster:** math-rust  
**Language:** Rust  
**Source:** [SuperInstance/aho-corasick-rs](https://github.com/SuperInstance/aho-corasick-rs)

## Intention

Aho-Corasick multi-pattern string matching and automaton construction

## How It Works

**Phase 1 — Trie construction:** Insert each pattern byte-by-byte into a trie. Each terminal node records which pattern(s) end there.

**Phase 2 — Failure links (BFS):** Starting from the root's children, perform a BFS. For each node `u` with character `c`:
- If `u` has a child for `c`, set that child's failure link to `goto[fail[u]][c]`.
- If `u` has no child for `c`, set `goto[u][c] = goto[fail[u]][c]`.

This "dangling edge" resolution means every state has a defined transition for every byte — no runtime failure-link chasing.

**Phase 3 — Output propagation:** During BFS, each node inherits

## What It's For

Aho-Corasick multi-pattern string matching and automaton construction

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (97 lines, 5805 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# aho-corasick-rs

[![crates.io](https://img.shields.io/crates/v/aho-corasick-rs.svg)](https://crates.io/crates/aho-corasick-rs)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

Aho-Corasick multi-pattern string matching automaton in pure Rust.

## The Problem

You need to search a text for **all occurrences** of multiple patterns simultaneously. Running a separate search per pattern is O(k · n) where k is the number of patterns and n is the text length. When k is large (e.g., a dictionary of 10,000 keywords), this becomes prohibitive.

## The Insight

The Aho-Corasick algorithm builds a single automaton from all patterns that processes the text in **one pass**. It combines two ideas:

1. **Trie structure** — All patterns share a common prefix tree, so matching "he" and "hers" shares the `h → e` prefix path.
2. **Failure links** — When the current character doesn't match any child, instead of restarting from the root, jump to the longest proper suffix of the current path that is also a trie prefix. This is analogous to KMP's failure function, but generalized to multiple patterns.

With a precomputed `goto` table (a 2D array indexed by `[state][byte]`), each character in the text causes exactly one state transition — O(1) per character, regardless of pattern count.

## How It Works

**Phase 1 — Trie construction:** Insert each pattern byte-by-byte into a trie. Each terminal node records which pattern(s) end there.

**Phase 2 — Failure links (BFS):** Starting from the root's children, perform a BFS. For each node `u` with character `c`:
- If `u` has a child for `c`, set that child's failure link to `goto[fail[u]][c]`.
- If `u` has no child for `c`, set `goto[u][c] = goto[fail[u]][c]`.

This "dangling edge" resolution means every state has a defined transition for every byte — no runtime failure-link chasing.

**Phase 3 — Output propagation:** During BFS, each node inherits the output list of its failure target. This ensures all pattern matches are reported without additional follow-up at search time.

**Search:** Walk the text one byte at a time. At each position, check the current state's output list for matches.

## Usage

```rust
use aho_corasick::{AhoCorasick, Match};

let ac = AhoCorasick::new(&["he", "she", "his", "hers"]);

// Find all matches
let matches: Vec<Match> = ac.find_all(b"ahishers");
assert_eq!(matches.len(), 4);
// Match { pattern_id: 2, start: 1, end: 4 }  — "his"
// Match { pattern_id: 1, start: 3, end: 6 }  — "she"
// Match { pattern_id: 0, start: 4, end: 6 }  — "he"
// Match { pattern_id: 3, start: 4, end: 8 }  — "hers"

// Quick checks
assert!(ac.contains(b"ahishers"));
assert_eq!(ac.count(b"banana"), 0);

// Byte-string patterns (non-UTF8)
let ac_bin = AhoCorasick::from_bytes(&[b"\x00\x01", b"\xff\xfe"]);
let matches = ac_bin.find_all(&[0x00, 0x01, 0xFF, 0xFE]);

// Metadata
println!("{} patterns, {} automaton states", ac.num_patterns(), ac.num_states());
```

## Module Map

Everything lives in
```
