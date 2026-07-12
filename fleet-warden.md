# fleet-warden

**URL:** https://github.com/SuperInstance/fleet-warden

## Intention
Automated disk cleanup daemon for WSL development environments. Based on real cleanup: 54 GB recovered.

## How It Works
Rust CLI/daemon scanning 7 categories: target dirs, pip/npm cache, old toolchains, stale sessions, HuggingFace weights, large files. Check (dry run), clean, watch (daemon), and budget modes.

## What It's For
Preventing WSL/dev environment disk bloat.

## Who Would Use It
Developers on WSL.

## Language/Stack
Rust

## Status Assessment
Active — practical with real usage data.

## Honest Assessment
Real project — genuinely practical tool solving a real problem (WSL disk bloat).
