# log-aggregator

## Intention

Centralized log aggregation and analysis service for distributed systems

## How It Works

**Aggregation model**: Each log entry is a `(level, message)` tuple. The aggregator maintains a `HashMap<String, usize>` counting entries per level:
```
Input: [("info", "started"), ("error", "failed"), ("info", "done")]
Output: {"info": 2, "error": 1}
```
**Time complexity**: O(N) for N log entries — single pass with O(1) HashMap insert/update per entry. Space: O(L) where L is the number of distinct levels (typically 4–6: TRACE, DEBUG, INFO, WARN, ERROR, FATAL).
**Extension to richer aggregation**: The level-counting pattern generalizes to:
- **Rate computation**: `error_rate = error_count / total_count`
- **Sliding window**: rotate counts over time windows (tumbling or hopping)
- **Histogram**: bucket by message pattern, not just level
- **Percentile tracking**: use t-digest or HDR histogram for latency distributions
**Comparison with production log aggregators**:
| System | Scope | Complexity |
|--------|-------|------------|
| This library | Level counting | O(N) |

## What It's For

Centralized log aggregation and analysis service for distributed systems

## Who Would Use It

DevOps engineers and system operators needing observability tooling.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (55 lines), includes examples.

- README length: 78 lines, 4288 characters
- Documented sections: Why It Matters, How It Works, Quick Start, API, Architecture Notes

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
