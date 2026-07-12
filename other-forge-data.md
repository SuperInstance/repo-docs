# forge-data

## Intention
Structured data decomposition into tiles for Plato agents.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
`forge-data` takes common data formats (CSV, JSON, TSV) and decomposes them into **DataTiles** — structured, schema-aware units that can be filtered, sorted, aggregated, and reconstructed.

Each tile carries:
- A unique ID (`Uuid`)
- A `DataKind` tag (CsvRow, JsonNode, TsvRow, etc.)
- A `HashMap<String, Value>` of field → value pairs
- An index (original position)
- A schema key (ordered field nam

## Who Would Use It
```toml
[dependencies]
forge-data = { git = "https://github.com/SuperInstance/forge-data" }
```

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (78 line README).

## Honest Assessment
Has documentation (78 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/forge-data](https://github.com/SuperInstance/forge-data)*
