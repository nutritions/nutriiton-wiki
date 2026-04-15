---
type: source
status: draft
topic: obsidian-codex-wiki-setup
updated: 2026-04-15
raw_note: "[[raw/processed/others/obsidian-codex-个人wiki配置记录]]"
related_entities:
  - "[[entities/Obsidian]]"
  - "[[entities/Codex]]"
  - "[[entities/Obsidian Web Clipper]]"
related_concepts:
  - "[[concepts/Obsidian + Codex 个人Wiki工作流]]"
related_sources:
  - "[[sources/Codex-env-代理配置与作用说明]]"
---

# Obsidian-Codex 个人 Wiki 配置记录

## 来源信息

- 原始记录：[[raw/processed/others/obsidian-codex-个人wiki配置记录]]
- 记录时间：2026-04-15

## 核心摘要

该记录给出了个人 Wiki 从模板初始化到 skills、目录结构、Web Clipper 路径配置与日常流程的最小闭环实践。

## 关键观点

- 工作流核心为：`raw/unprocessed -> ingest_raw -> 审阅 -> approve_ingest`。
- Web Clipper 保存路径应使用 Vault 相对路径 `raw/unprocessed`，而非绝对磁盘路径。
- 项目语境统一与技能同步（项目内 + 全局）有助于跨工作区稳定使用。

## 证据摘录

- 已配置目录：`raw/{unprocessed,processed,assets}` 与 `wiki/{sources,entities,concepts,synthesis}`。
- 推荐插件包含 `Templater`、`Dataview`、`Custom Attachment Location` 等。

## 待确认问题

- 不同前端界面对中文文件名路径的跳转兼容性差异。