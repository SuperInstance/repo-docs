# Wiki Migration Plan

**Objective**: Archive 4 stale wiki repositories and deploy UNIFIED-WIKI.md as the single source of truth for the SuperInstance ecosystem.

---

## Status Quo

### Current Wiki Repositories

| Repository | Files | Status | Issues |
|------------|-------|--------|--------|
| **superinstance-wiki** | 551 | Stale | Superseded, outdated content |
| **wiki** | 3 | Stale | Placeholder, minimal content |
| **knowledge-agent** | 11 | Superseded | Replaced by PLATO knowledge system |
| **fleet-wiki** | 11 | Stale | Fleet docs, no longer maintained |

### Issues with Current Wikis

1. **Fragmentation** — Knowledge scattered across 4 repos
2. **Staleness** — None actively maintained, outdated information
3. **Duplication** — Overlapping content, inconsistent versions
4. **Accessibility** — No single entry point for new users
5. **Maintenance** — Updating requires changes in 4 places

---

## Migration Strategy

### Phase 1: Preparation ✅ (Complete)

- [x] Fetch READMEs and directory listings from all 4 wikis
- [x] Analyze existing content structure
- [x] Read MASTER-INDEX.md and ECOSYSTEM-ANALYSIS.md
- [x] Create UNIFIED-WIKI.md with consolidated content
- [x] Create WIKI-MIGRATION-PLAN.md

### Phase 2: Review (Recommended)

Before archiving, review the unified wiki:

1. **Read UNIFIED-WIKI.md** — Verify completeness and accuracy
2. **Check Links** — Ensure all references point to valid locations
3. **Validate repo-docs** — Confirm MASTER-INDEX.md and ECOSYSTEM-ANALYSIS.md are current
4. **Test Navigation** — Verify a new user can find what they need

### Phase 3: Archive Old Wikis

For each stale wiki repository:

1. **Update README.md** with archive notice:

```markdown
# ARCHIVED: This repository has been deprecated

**Status**: Archived — Content migrated to unified documentation

**Migration**: This wiki has been consolidated into the SuperInstance unified documentation system.

**New Location**: See [repo-docs](https://github.com/SuperInstance/repo-docs) for:
- UNIFIED-WIKI.md — Single source of truth for the ecosystem
- MASTER-INDEX.md — Complete repository catalog
- ECOSYSTEM-ANALYSIS.md — Deep architectural analysis

**Date Archived**: 2026-07-12
**Reason**: Consolidation of 4 stale wikis into a unified documentation system

---

## Historical Content

For historical reference, key content from this wiki has been preserved in the unified documentation:

- [Extracted Content Summary](#extracted-content)

## Repository Status

This repository is read-only and no longer maintained. Please use the unified documentation.
```

2. **Add extracted content section** — For each wiki, document what was extracted:

#### superinstance-wiki
- CATALOG.md content → Integrated into Repository Guide section
- ARCHITECTURE.md content → Integrated into Key Concepts
- GETTING-STARTED.md content → Integrated into Getting Started
- DASHBOARD.md content → Referenced in repo-docs

#### wiki
- ecosystem-catalog.md → Referenced in MASTER-INDEX.md
- capacities.md → Referenced in repo-docs
- autobiography.md → Preserved for historical reference

#### knowledge-agent
- Core concepts → Referenced in PLATO section
- API reference → Available in individual repo docs
- Architecture → Integrated into Key Concepts

#### fleet-wiki
- Fleet documentation → Integrated into Fleet Orchestration section
- API documentation → Preserved in individual repo docs
- CLI reference → Available in individual repo docs

3. **Archive the repository**:

```bash
# For each wiki repo:
gh repo edit SuperInstance/REPO-NAME --archived true
```

4. **Create a pinned issue** pointing to new location:

```markdown
# 📌 Archived: Content Moved

This repository has been archived. All documentation has been consolidated into the [SuperInstance unified documentation](https://github.com/SuperInstance/repo-docs).

## New Location

📖 **[UNIFIED-WIKI.md](https://github.com/SuperInstance/repo-docs/blob/main/UNIFIED-WIKI.md)** — The single source of truth for the SuperInstance ecosystem.

## What Changed

- 4 separate wikis → 1 unified documentation system
- Stale content removed or updated
- Single entry point for new users
- Consistent information across all docs

## Questions?

Open an issue in [repo-docs](https://github.com/SuperInstance/repo-docs/issues).
```

### Phase 4: Deploy Unified Wiki

#### Option A: Create Dedicated Wiki Repo

Create a new `superinstance-docs` repository:

1. **Create repository**:
```bash
gh repo create SuperInstance/superinstance-docs --public --description "Unified documentation for the SuperInstance ecosystem"
```

2. **Populate with content**:
- UNIFIED-WIKI.md (rename to README.md or index.md)
- MASTER-INDEX.md
- ECOSYSTEM-ANALYSIS.md
- Individual repo docs (if desired)

3. **Configure GitHub Pages** (optional):
```bash
# Enable GitHub Pages for the new repo
gh api repos/SuperInstance/superinstance-docs/pages --method put -f source.branch=main -f source.path=/
```

#### Option B: Use Existing repo-docs

If `repo-docs` already exists and is accessible:

1. **Ensure files are in place**:
- UNIFIED-WIKI.md ✅
- MASTER-INDEX.md ✅
- ECOSYSTEM-ANALYSIS.md ✅

2. **Make repo-docs public** (if private):
```bash
gh repo edit SuperInstance/repo-docs --visibility public
```

3. **Update repo-docs README** to point to UNIFIED-WIKI.md as entry point

4. **Pin repo-docs** to organization profile

### Phase 5: Organization Updates

1. **Update Organization Description** (if applicable):
```
SuperInstance: Autonomous AI systems grounded in mathematical physics and conservation laws.

Documentation: [repo-docs](https://github.com/SuperInstance/repo-docs)
```

2. **Update Organization README** (if exists):
- Link to UNIFIED-WIKI.md as primary documentation
- Archive old wiki links
- Add migration notice

3. **Update Internal Links**:
- Search codebase for links to old wikis
- Replace with links to unified docs or individual repo docs

---

## Post-Migration Checklist

- [ ] All 4 wikis archived with README notices
- [ ] UNIFIED-WIKI.md publicly accessible
- [ ] MASTER-INDEX.md and ECOSYSTEM-ANALYSIS.md accessible
- [ ] Organization profile updated
- [ ] Internal links updated
- [ ] Team notified of new documentation location
- [ ] Old wiki URLs redirect (if using custom domain)

---

## Rollback Plan

If migration needs to be undone:

1. **Unarchive repositories**:
```bash
gh repo edit SuperInstance/REPO-NAME --archived false
```

2. **Restore original READMEs** (if saved)

3. **Update organization links** back to old wikis

---

## Estimated Effort

| Phase | Time | Effort |
|-------|------|--------|
| Preparation | ✅ Complete | Done |
| Review | 30 min | Low |
| Archive Old Wikis | 1 hour | Low |
| Deploy Unified Wiki | 30 min | Low |
| Organization Updates | 30 min | Low |
| **Total** | **2.5 hours** | **Low** |

---

## Benefits of Migration

| Before | After |
|--------|-------|
| 4 fragmented wikis | 1 unified documentation |
| Stale content | Current, accurate information |
| No single entry point | Clear navigation for new users |
| Maintenance in 4 places | Single source of truth |
| Conflicting information | Consistent documentation |

---

## Questions & Answers

**Q: What happens to the content from old wikis?**
A: All valuable content has been extracted and integrated into UNIFIED-WIKI.md, MASTER-INDEX.md, or preserved in individual repo docs.

**Q: Can old wikis still be accessed?**
A: Yes, they're archived (read-only) with notices pointing to the new location.

**Q: What if someone finds an old link?**
A: Archived repos have README notices directing to the new documentation.

**Q: Will this be done automatically?**
A: No, this plan requires manual execution with `gh` CLI or GitHub web interface.

---

*Plan created: 2026-07-12*
*Ready for execution upon approval*
