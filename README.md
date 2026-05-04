# ruflo-knowledge-keeper

Lightweight AI memory for Ruflo agents — 32 MCP tools, zero API keys, Obsidian compatible.

Unlike ruflo-agentdb (which requires vector DB + embeddings API), Knowledge Keeper runs with **zero external dependencies**. All data stored as human-readable Markdown in an Obsidian-compatible vault.

## Install

```
/plugin marketplace add ruvnet/ruflo
/plugin install ruflo-knowledge-keeper@ruflo
```

Or add as MCP server directly:

```json
{
  "mcpServers": {
    "knowledge-keeper": {
      "command": "npx",
      "args": ["-y", "@zsc-glitch/knowledge-keeper-mcp@1.6.0"]
    }
  }
}
```

## Features

- **32 MCP tools** — Complete knowledge management
- **Zero API keys** — No OpenAI, no embeddings API, everything local
- **Hybrid search** — BM25 (R@5=95%) + TF-IDF semantic + RRF fusion
- **Knowledge graph** — Entity detection, relationships, Mermaid visualization
- **Duplicate detection** — Find and merge similar knowledge points
- **Obsidian compatible** — Read/write with Obsidian vault
- **Audit trail** — SHA256 hash chain, integrity verification
- **Version history** — Diff & rollback any change
- **313 KB** — Lightweight, no native dependencies

## vs ruflo-agentdb

| Feature | Knowledge Keeper | ruflo-agentdb |
|---------|-----------------|---------------|
| API keys needed | ❌ Zero | ✅ ONNX embeddings |
| Native dependencies | ❌ None | ✅ better-sqlite3 |
| Package size | 313 KB | Heavy stack |
| Obsidian compatible | ✅ | ❌ |
| Audit trail | ✅ SHA256 | ✅ AttestationLog |
| Duplicate detection | ✅ | ❌ |
| Install complexity | `npx` one-liner | Multi-step setup |

## Skills

- **knowledge-save** — Save and categorize knowledge
- **knowledge-search** — Search with BM25, semantic, or hybrid

## Setup

First run automatically creates the vault at `~/.knowledge-vault/` with Obsidian-compatible structure.
