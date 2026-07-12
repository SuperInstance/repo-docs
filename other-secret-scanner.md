# secret-scanner

## Intention
Git history secret scanner — detect accidentally committed credentials across fleet repos

## How It Works
Scans all fleet repositories for accidentally committed secrets and sensitive data. Unlike outbound leak detectors (which inspect network traffic), this tool checks git history — finding secrets that were committed at any point in time, even if they were later removed. - Current files: Scan all files in the working directory - Git history: Walk git log -p to find secrets in every commit - Diff scan: Scan uncommitted changes (git diff) - Staged scan: Scan the staging area (git diff --cached) - Baseline drift: Save a snapshot and detect NEW secrets over time Secret Patterns Detected

## What It's For
Git history secret scanner — detect accidentally committed credentials across fleet repos

## Who Would Use It
Python developers building AI agent fleets

## Language / Stack
Python

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 3,404 characters, 113 lines
- Code examples: 4 blocks
- Installation instructions: yes
- Testing mentioned: yes
- License mentioned: no
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (4 code blocks)
- Installation/usage instructions provided
- Testing mentioned

**Concerns:**
- None immediately apparent from README alone

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
