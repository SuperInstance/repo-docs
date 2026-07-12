# local-vector-search

## Intention

Local TF-IDF vector search engine for repo discovery

## How It Works

```
Document    → represents a repo with text features (name, readme, deps, extensions)
Index       → builds a TF-IDF index over all documents
Searcher    → cosine similarity search returning top-K results
QueryBuilder→ natural language queries ("find me graph libraries with tests")
IndexBuilder→ scans a directory, builds the index, serializes to binary
Benchmarker → measures query latency, index build time, memory usage
```
### Feature Extraction
For each repo, the `IndexBuilder` extracts:
- **Name** — the directory name itself
- **README** — first 2000 chars of README.md/README.txt
- **Dependencies** — parsed from Cargo.toml, package.json, requirements.txt
- **File extensions** — all unique extensions found in the repo
- **Key files** — presence of main.rs, lib.rs, tests/, examples/, etc.

## What It's For

Local TF-IDF vector search engine for repo discovery

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (103 lines), mentions tests, includes examples, has benchmarks.

- README length: 139 lines, 4221 characters
- Documented sections: Results (609 repos, real benchmark), Architecture, Usage, Performance, Dependencies

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
