# lighthouse

## Intention

Fleet Lighthouse — unified health dashboard, alerting, diagnostics for Pelagic fleet

## How It Works

```bash
# Start live dashboard
python cli.py serve
# One-shot status check
python cli.py status
# View health history
python cli.py history "Keeper Agent"
# View alerts
python cli.py alerts --all
# Export data
python cli.py export --format json
python cli.py export --component "Trail Agent" --format csv --output trail.csv
# Run diagnostics
python cli.py doctor
```

## What It's For

Fleet Lighthouse — unified health dashboard, alerting, diagnostics for Pelagic fleet

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Python

## Status Assessment

**Status: LIGHT**

Short README (45 lines), mentions tests, includes examples.

- README length: 59 lines, 1807 characters
- Documented sections: Files, Usage, Components Monitored, Health Status Transitions

## Honest Assessment

Some documentation exists but it's not comprehensive. The project may have working code, but the README doesn't provide enough evidence of maturity, testing, or real-world use. **Promising direction, needs more evidence of substance.**
