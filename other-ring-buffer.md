# ring-buffer

## Intention
Audio pipeline NaN guard — fixed-length ring buffer with sanitisation

## How It Works
[](https://pypi.org/project/ring-buffer/) [](https://www.python.org/downloads/) Audio pipeline NaN guard. A fixed-length ring buffer for real-time audio streams that silently replaces NaN / ±Inf with 0.0 on push. Extracted from the OpenSMILE bridge NaN fix — the exact guard that prevents silent corruption when downstream feature extractors (MFCC, prosody, etc.) encounter non-finite samples.

## What It's For
Audio pipeline NaN guard — fixed-length ring buffer with sanitisation

## Who Would Use It
Python developers

## Language / Stack
Python

## Status Assessment
**Developing** — Moderate documentation with some structure and examples.

- README size: 2,719 characters, 95 lines
- Code examples: 5 blocks
- Installation instructions: yes
- Testing mentioned: yes
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: no

## Honest Assessment

**Strengths:**
- Code examples present (5 code blocks)
- Installation/usage instructions provided
- Testing mentioned

**Concerns:**
- None immediately apparent from README alone

**Overall:** Early but potentially interesting — read the source to verify.
