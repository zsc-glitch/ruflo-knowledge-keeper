---
name: kk
description: Knowledge Keeper — save, search, and manage persistent AI memory. Zero API keys, Obsidian compatible.
argument-hint: "<action> [query]"
allowed-tools: mcp__knowledge-keeper__knowledge_save mcp__knowledge-keeper__knowledge_search mcp__knowledge-keeper__knowledge_hybrid_search mcp__knowledge-keeper__knowledge_bm25_search mcp__knowledge-keeper__knowledge_recent mcp__knowledge-keeper__knowledge_get mcp__knowledge-keeper__knowledge_update mcp__knowledge-keeper__knowledge_delete mcp__knowledge-keeper__knowledge_tags mcp__knowledge-keeper__knowledge_link mcp__knowledge-keeper__knowledge_duplicates mcp__knowledge-keeper__knowledge_merge mcp__knowledge-keeper__knowledge_export mcp__knowledge-keeper__knowledge_review mcp__knowledge-keeper__knowledge_analytics_overview mcp__knowledge-keeper__knowledge_audit Bash
---

# Knowledge Keeper Command

Manage your AI agent's persistent memory with Knowledge Keeper MCP.

## Usage

`/kk save` — Save a new knowledge point
`/kk search <query>` — Hybrid search across all knowledge
`/kk recent` — Show recently added/updated knowledge
`/kk duplicates` — Find similar/duplicate knowledge points
`/kk review` — Spaced repetition review scheduler
`/kk stats` — Knowledge base overview and analytics
`/kk audit` — Verify knowledge base integrity (SHA256)

## Quick Start

After first use, Knowledge Keeper creates `~/.knowledge-vault/` with Obsidian-compatible Markdown structure.

No API keys needed. No cloud required. Everything runs locally.
