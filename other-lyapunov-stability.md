# lyapunov-stability

## Intention

Lyapunov stability analysis for agent systems

## How It Works

```python
from lyapunov_stability import LyapunovAnalyzer
analyzer = LyapunovAnalyzer()
# Analyze V = x^2 + y^2 (stable paraboloid)
result = analyzer.analyze(
V=lambda x, y: x**2 + y**2,
dVdx=lambda x, y: 2*x,
dVdy=lambda x, y: 2*y,
equilibrium=(0.0, 0.0),
)
print(result.stability)           # STABLE
print(result.is_positive_definite) # True
print(result.basin_radius)        # 4.99+ (large basin)
```
Supports 2D systems. Analytical or numerical gradients. Central difference approximation.

## What It's For

Lyapunov stability analysis for agent systems

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Python

## Status Assessment

**Status: LIGHT**

Short README (20 lines), includes examples.

- README length: 29 lines, 849 characters
- Documented sections: Usage

## Honest Assessment

Some documentation exists but it's not comprehensive. The project may have working code, but the README doesn't provide enough evidence of maturity, testing, or real-world use. **Promising direction, needs more evidence of substance.**
