# granger-causality

## Intention
**Granger causality testing with vector autoregression (VAR), lag selection via AIC/BIC, and impulse response analysis.**

## How It Works
```rust
use granger_causality::*;

// Two time series
let y1: Vec<f64> = (0..100).map(|i| i as f64).collect();
let y2: Vec<f64> = (0..100).map(|i| 2.0 * i as f64).collect();

// Fit VAR(2) model
let model = VARModel::fit(&[y1, y2], 2);
println!("Lag order: {}", model.lag());
println!("RSS for equation 1: {:.4}", model.rss(0));
println!("RSS for equation 2: {:.4}", model.rss(1));

// Forecast one step ahead
let past = vec![vec![99.0, 98.0], vec![198.0, 196.0]]; // [var][lag_idx]
let forecast = mo

## What It's For
**Granger causality** is a statistical hypothesis test for determining whether one time series is useful in forecasting another. A time series X Granger-causes Y if past values of X contain statistically significant information about future values of Y, beyond what Y's own past values provide.

This is **not** true causality in the philosophical sense — it's about **predictive precedence**. Howeve

## Who Would Use It
```toml
[dependencies]
granger-causality = "0.1.0"
```

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (186 line README).

## Honest Assessment
Moderately documented (186 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/granger-causality](https://github.com/SuperInstance/granger-causality)*
