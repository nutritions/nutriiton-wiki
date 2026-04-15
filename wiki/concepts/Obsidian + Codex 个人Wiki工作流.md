---
type: concept
status: draft
topic: personal-wiki-workflow
updated: 2026-04-15
supports:
  - "[[sources/Obsidian-Codex-个人Wiki配置记录]]"
related_entities:
  - "[[entities/Obsidian]]"
  - "[[entities/Codex]]"
  - "[[entities/Obsidian Web Clipper]]"
related_sources:
  - "[[sources/Obsidian-Codex-个人Wiki配置记录]]"
---

# Obsidian + Codex 个人Wiki工作流

## 定义

将对话知识与外部资料持续沉淀为本地 wiki 的工作方法。

## 标准流程

1. 新资料进入 `raw/unprocessed`。
2. 执行 `ingest_raw` 沉淀到 `wiki`。
3. 人工审阅后执行 `approve_ingest`。
4. 日常通过 `query_wiki` 使用，必要时 `inspool` 回填。

## 关键实践

- Web Clipper 使用相对路径。
- 先保证记录落到 raw，再进入结构化沉淀。
- 通过 `lint_wiki` 定期纠偏。