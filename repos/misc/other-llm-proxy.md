# llm-proxy

## Intention

Remote language oracle for spreadsheet cells — calls DeepInfra Seed-2.0-mini

## How It Works

**Architecture**:
```
Spreadsheet Engine
↓  POST /oracle {cell_id, tick, value, neighbors, phase}
LLM Proxy (this)
↓  Construct prompt
↓  Rate limit check (sliding window)
↓  POST to DeepInfra API
DeepInfra Seed-2.0-mini
↓  Returns chat completion
LLM Proxy
↓  Parse response → extract float
↓  Return {cell_id, tick, oracle_value}
Spreadsheet Engine
```

## What It's For

Remote language oracle for spreadsheet cells — calls DeepInfra Seed-2.0-mini

## Who Would Use It

Machine learning engineers and researchers. Teams deploying or managing ML models.

## Language / Stack

- **Primary language:** Python

## Status Assessment

**Status: MODERATE**

Reasonable README (88 lines), mentions tests, includes examples.

- README length: 114 lines, 4502 characters
- Documented sections: Why It Matters, How It Works, Quick Start, API, Architecture Notes

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
