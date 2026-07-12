# Claude-prism-local-json

**Cluster:** typescript-misc  
**Language:** TypeScript  
**Source:** [SuperInstance/Claude-prism-local-json](https://github.com/SuperInstance/Claude-prism-local-json)

## Intention

Local JSON version of PRISM.

## How It Works

**Vectorizing** = converting text into numbers that capture meaning

Think of it like coordinates on a map:
- "cat" and "dog" are close together (both animals)
- "car" and "truck" are close together (both vehicles)
- "login" and "authentication" are close together (both security concepts)

PRISM breaks your code into chunks, vectorizes them, and stores them in a **vector database**. When you search "how users log in," it finds code chunks with similar vectors - **even if the words don't match exactly**.

### Where Everything Lives

| Component | What It Stores | Where |
|-----------|----------

## What It's For

Local JSON version of PRISM.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

TypeScript — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (635 lines, 14844 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# PRISM

> **Search code by meaning, not keywords - so AI assistants give you correct answers in seconds instead of hours.**

---

## The Problem: You're Working in a Large Codebase

You want Claude to help you fix a bug or add a feature. But you can only give Claude 128K tokens of context. Your codebase is millions of tokens.

**What do you do?**

### The Old Way
```
1. Grep codebase for hours
2. Copy-paste random files into Claude
3. Hope Claude has what it needs
4. Claude: "I don't have enough context"
5. Copy 20 MORE files
6. Claude gives wrong answer because it missed a critical file
7. You waste 4 hours
```

### The PRISM Way
```
You: "prism search 'user login flow'"
PRISM: Returns 5 most relevant code chunks (not files, CHUNKS)
You: Paste those chunks into Claude
Claude: Has perfect context → gives you the right answer
```

---

## What PRISM Does (In 30 Seconds)

**PRISM** is a semantic code search engine that helps you find code by **meaning**, not just keywords.

### How It Works

**Vectorizing** = converting text into numbers that capture meaning

Think of it like coordinates on a map:
- "cat" and "dog" are close together (both animals)
- "car" and "truck" are close together (both vehicles)
- "login" and "authentication" are close together (both security concepts)

PRISM breaks your code into chunks, vectorizes them, and stores them in a **vector database**. When you search "how users log in," it finds code chunks with similar vectors - **even if the words don't match exactly**.

### Where Everything Lives

| Component | What It Stores | Where |
|-----------|---------------|-------|
| **Vectorize** | 384-dimensional vectors (embeddings) | Cloudflare's edge (global) |
| **D1 Database** | File metadata, SHA-256 checksums, chunk content | Cloudflare's edge (global) |
| **R2 Storage** | Raw files (optional) | Cloudflare's edge (global) |
| **KV Cache** | Embedding cache (avoid regenerating) | Cloudflare's edge (global) |

**Key point:** Everything lives on Cloudflare's edge. Fast. Cheap. No infrastructure to manage.

---

## How It Fits Your Workflow

### Before PRISM
```
1. Find bug in production
2. Grep codebase for hours
3. Copy 20 files into Claude
4. Claude: "I don't have enough context"
5. Copy 20 MORE files
6. Claude gives wrong answer because it missed a critical file
7. You waste 4 hours
```

### With PRISM
```
1. Find bug in production
2. prism search "user authentication error"
3. Get 5 relevant chunks in 50ms
4. Paste into Claude
5. Claude gives correct answer immediately
6. You fix it in 20 minutes
```

---

## The ROI: Time, Money, Quality

### Time Saved
- **Code search:** From hours to milliseconds
- **Context gathering:** From manual file hunting to automatic semantic search
- **Debugging:** 50-80% faster because Claude has the right code

### Money Saved
- **Claude API costs:** 90% reduction (only send relevant chunks, not entire codebase)
- **Development time:** Faster debugging = ship features faster
- **Infrastructure 
```
