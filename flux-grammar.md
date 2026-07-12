# flux-grammar

**Category:** 🔧 Toolchain
**Status:** 🟡 Development
**Language:** Python
**README:** 1,001 bytes

## Intention
Formal FLUX assembly language grammar — lexer, parser, validator

## How It Works
- **Lexer**: Tokenizes source into OPCODE, REGISTER, IMMEDIATE, LABEL_DEF, COMMENT tokens
- **Parser**: Builds AST with InstructionNode, LabelNode, ProgramNode
- **Validator**: Checks operand counts and types against opcode signatures

## Language Reference

```
program     = { line }
line        = label | instruction | comment | blank
instruction = opcode { operand }
operand     = register | immediate
register    = "R" digit+
immediate   = ["-"] decimal | "0x" hex
comment     = ";" text
```

##...

## What It's For
Formal FLUX assembly language grammar — lexer, parser, validator

## Who Would Use It
Developers in the FLUX ecosystem.

## Honest Assessment
Has code examples. claims 16 tests. missing: tests, benchmarks.
