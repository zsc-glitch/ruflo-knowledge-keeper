---
name: knowledge-save
description: Save knowledge points with type, tags, and links. Use when you need to persist information, decisions, concepts, or notes for later recall.
argument-hint: "<type> <title> <content>"
allowed-tools: mcp__knowledge-keeper__knowledge_save mcp__knowledge-keeper__knowledge_get mcp__knowledge-keeper__knowledge_link mcp__knowledge-keeper__knowledge_tags Bash
---

# Knowledge Save

Save and categorize knowledge points for persistent memory across sessions.

## When to use

When you need to remember information for later: decisions, concepts, todos, notes, or project records. Knowledge is stored as Obsidian-compatible Markdown files and indexed for instant search.

## Steps

1. **Choose type** — Select from: concept, decision, todo, note, project
2. **Save knowledge** — call `mcp__knowledge-keeper__knowledge_save` with type, title, content, and optional tags
3. **Add tags** — include relevant tags for easy retrieval
4. **Link related** — call `mcp__knowledge-keeper__knowledge_link` to connect to existing knowledge points

## Examples

Save a concept:
```
mcp__knowledge-keeper__knowledge_save({
  type: "concept",
  title: "React Server Components",
  content: "RSC allows server-side rendering with 'use server' directive...",
  tags: ["react", "frontend", "ssr"]
})
```

Save a decision:
```
mcp__knowledge-keeper__knowledge_save({
  type: "decision",
  title: "Choose Redis over Memcached",
  content: "Selected Redis for data structures, persistence, and pub/sub support...",
  tags: ["redis", "cache", "architecture"]
})
```

## CLI alternative

```bash
npx @zsc-glitch/knowledge-keeper-mcp
```
