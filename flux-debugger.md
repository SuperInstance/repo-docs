# flux-debugger

**Category:** 📊 Testing/Profiling
**Status:** 🟡 Development
**Language:** Python
**README:** 3,176 bytes

## Intention
FLUX step debugger with breakpoints, reverse stepping, and state inspection

## How It Works
```python
from flux_debugger import FluxDebugger, Breakpoint, BreakpointType

dbg = FluxDebugger([0x18, 0, 5, 0x18, 1, 1, 0x22, 1, 1, 0,
                     0x09, 0, 0x3D, 0, -6, 0, 0x00])  # factorial(5)

# Set breakpoints
dbg.add_breakpoint(Breakpoint(BreakpointType.PC, value=6))     # before MUL
dbg.add_breakpoint(Breakpoint(BreakpointType.OP, value=0x22))  # any MUL
dbg.add_breakpoint(Breakpoint(BreakpointType.REGISTER, value=0,
                               register=0, condition="eq"))   ...

## What It's For
FLUX step debugger with breakpoints, reverse stepping, and state inspection

## Who Would Use It
Developers in the FLUX ecosystem.

## Honest Assessment
Has code examples. missing: tests, benchmarks.
