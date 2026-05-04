---
name: knowledge-search
description: Search knowledge with BM25 keyword, TF-IDF semantic, or hybrid RRF fusion. Use when you need to recall previously saved information.
argument-hint: "<query>"
allowed-tools: mcp__knowledge-keeper__knowledge_search mcp__knowledge-keeper__knowledge_bm25_search mcp__knowledge-keeper__knowledge_semantic_search mcp__knowledge-keeper__knowledge_hybrid_search mcp__knowledge-keeper__knowledge_recent mcp__knowledge-keeper__knowledge_duplicates Bash
---

# Knowledge Search

Search and retrieve knowledge points with multiple search strategies.

## When to use

When you need to find previously saved knowledge: concepts, decisions, notes, or any stored information.

## Search strategies

1. **BM25 keyword search** — Best for exact term matching. Call `mcp__knowledge-keeper__knowledge_bm25_search` with query terms. R@5=95%.

2. **Semantic search** — Best for conceptual matching. Call `mcp__knowledge-keeper__knowledge_semantic_search` with natural language query. TF-IDF based, no API needed.

3. **Hybrid search (recommended)** — Combines BM25 + semantic with RRF fusion. Call `mcp__knowledge-keeper__knowledge_hybrid_search` for best results.

4. **Recent knowledge** — List recently added/updated entries. Call `mcp__knowledge-keeper__knowledge_recent` with optional sort_by, days, type filters.

5. **Duplicate detection** — Find similar knowledge points. Call `mcp__knowledge-keeper__knowledge_duplicates` with threshold and scope.

## Steps

1. **Choose strategy** — Use hybrid for best results, BM25 for exact matches
2. **Search** — call the appropriate search tool with your query
3. **Get full entry** — call `mcp__knowledge-keeper__knowledge_get` with the ID for complete content
4. **Find duplicates** — call `mcp__knowledge-keeper__knowledge_duplicates` to detect similar entries

## Examples

Hybrid search:
```
mcp__knowledge-keeper__knowledge_hybrid_search({
  query: "caching strategy for API",
  limit: 5
})
```

Recent knowledge (last 7 days):
```
mcp__knowledge-keeper__knowledge_recent({
  days: 7,
  limit: 10,
  sort_by: "updated"
})
```

Find duplicates:
```
mcp__knowledge-keeper__knowledge_duplicates({
  threshold: 0.7,
  scope: "both"
})
```
