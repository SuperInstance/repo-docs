# flux-site

**Category:** 📚 Docs/Research
**Status:** 🟡 Development
**Language:** HTML
**README:** 1,111 bytes

## Intention
FLUX community site: playground, benchmarks, timeline, PHP kit. Deploy at cocapn.ai. Apache 2.0.

## How It Works
```php
<?php
require_once 'php-kit/flux-tiles.php';
require_once 'php-kit/flux-compiler.php';
// See php-kit/examples/ for full examples
```

## Deployment

```bash
docker build -t flux-site .
docker run -p 8080:80 flux-site
```

## License

Apache-2.0 — see [LICENSE](LICENSE).

## What It's For
FLUX community site: playground, benchmarks, timeline, PHP kit. Deploy at cocapn.ai. Apache 2.0.

## Who Would Use It
Developers in the FLUX ecosystem.

## Honest Assessment
Has code examples. missing: tests, CI.
