# flux-conformance

**Category:** ✅ Constraint/Safety
**Status:** 🟢 Production-oriented
**Language:** Python
**README:** 3,947 bytes

## Intention
FLUX Ecosystem - flux-conformance

## How It Works
```
T-002-flux-conformance/
├── conformance_suite.py         # Main test runner + pytest integration
├── bytecode_fixtures.py         # Hand-crafted bytecode programs with expected results
├── runtime_adapters/
│   ├── abstract_adapter.py      # Interface all runtimes must implement
│   ├── python_adapter.py        # flux-runtime Python adapter
│   └── c_adapter.py             # flux-runtime-c C11 adapter
├── test_categories/
│   ├── test_encoding.py         # Instruction encoding/decoding confo...

## What It's For
FLUX Ecosystem - flux-conformance

## Who Would Use It
Developers in the FLUX ecosystem.

## Honest Assessment
Has real code examples and installation instructions. missing: benchmarks.
