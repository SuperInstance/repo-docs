# prompt-compiler

## Intention
Compile, compose, validate, and version prompt templates for LLM workflows

## How It Works
A Rust library for compiling, composing, validating, and versioning prompt templates for LLM workflows. - PromptTemplate — Templates with {{variable}} placeholders and typed variables (string, number, enum) - PromptComposer — Compose multiple templates into a pipeline (parallel or chained) - TokenBudget — Estimate token counts, enforce limits, and auto-truncate - PromptValidator — Catch missing variables, circular references, empty sections, and excessive length - PromptVersion — Versioned templates with diffs between versions (added/removed/changed sections) - PromptCompiler — Compile a template tree into a final prompt string with all variables filled In chained mode, each stage's output is available as {{previous_output}} for the next:

## What It's For
Compile, compose, validate, and version prompt templates for LLM workflows

## Who Would Use It
Rust developers

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 5,510 characters, 187 lines
- Code examples: 9 blocks
- Installation instructions: no
- Testing mentioned: no
- License mentioned: yes
- API documentation: no
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (9 code blocks)
- Solid README with good coverage

**Concerns:**
- No clear installation instructions

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
