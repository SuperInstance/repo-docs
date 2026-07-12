# auto-changelog

**Cluster:** logging-business  
**Language:** Rust  
**Source:** [SuperInstance/auto-changelog](https://github.com/SuperInstance/auto-changelog)

## Intention

Automatic changelog generator from conventional commits

## How It Works

[code]

## What It's For

Automatic changelog generator from conventional commits

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (217 lines, 6269 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# auto-changelog

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Language: Rust](https://img.shields.io/badge/language-Rust-orange.svg)]()
[![SuperInstance](https://img.shields.io/badge/part%20of-SuperInstance-9cf.svg)](https://github.com/SuperInstance)

Automatic changelog generator from conventional commits. Parses `git log`, classifies commits by [Conventional Commits](https://www.conventionalcommits.org/) format, computes semver bumps, and outputs grouped markdown changelogs and release notes.

## Overview

Every repo in the SuperInstance ecosystem follows conventional commits. `auto-changelog` turns those commit messages into structured changelogs without any manual input. It reads your git history, classifies each commit, determines the next version number, and generates markdown.

No config files. No templates. Just run it against any repo that uses conventional commits.

## Installation

```bash
cargo install --path .
```

Dependencies: `clap` (CLI), `regex` (parsing), `semver`, `chrono`, `serde`/`serde_json` (types).

## Usage

```bash
# Generate full changelog to stdout
auto-changelog changelog

# Write changelog to a file
auto-changelog changelog --output CHANGELOG.md

# Include all history (not just since last tag)
auto-changelog changelog --all

# What's the next version?
auto-changelog next-version

# Generate release notes for the latest version
auto-changelog release-notes --output RELEASE.md

# Check last 20 commits for conventional compliance
auto-changelog check

# Check last 50 commits
auto-changelog check --count 50
```

Point at a different repo with `-r`:

```bash
auto-changelog -r /path/to/repo changelog
```

## Architecture

```
┌──────────────────────────────────────────────┐
│                   main.rs                     │
│            CLI (clap Parser)                  │
├──────────────────────────────────────────────┤
│ git_parser.rs    → RawCommit                  │
│    parse_log(), last_tag(), tags()            │
├──────────────────────────────────────────────┤
│ commit_classifier.rs → ClassifiedCommit       │
│    classify(), classify_all()                 │
├──────────────────────────────────────────────┤
│ version_bumper.rs  → VersionGroup             │
│    bump(), group_by_version()                 │
├──────────────────────────────────────────────┤
│ changelog_generator.rs → Markdown string      │
│    generate()                                 │
├──────────────────────────────────────────────┤
│ release_notes.rs → Release notes markdown     │
│    generate()                                 │
├──────────────────────────────────────────────┤
│ conventional_checker.rs → CheckResult[]       │
│    check()                                    │
└──────────────────────────────────────────────┘
```

## API Reference

### Types (`types.rs`)

```rust
pub struct RawCommit {
    pub hash: String,
    pub author: String,
    pub date: String,
    pub message: String,
}

pub enum CommitTyp
```
