# mac-digest

## Intention

A pure-Rust implementation of Message Authentication Code (MAC) algorithms with no external dependencies.

## How It Works

```rust
use mac_digest::hmac::Hmac;
let key = b"secret-key";
let message = b"hello world";
let tag = Hmac::compute(key, message);
assert!(Hmac::verify(key, message, &tag));
```

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. A pure-Rust implementation of Message Authentication Code (MAC) algorithms with no external dependencies.

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: LIGHT**

Short README (20 lines), mentions tests, includes examples.

- README length: 30 lines, 730 characters
- Documented sections: Features, Usage, Test Coverage

## Honest Assessment

Some documentation exists but it's not comprehensive. The project may have working code, but the README doesn't provide enough evidence of maturity, testing, or real-world use. **Promising direction, needs more evidence of substance.**
