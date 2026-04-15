---
source_type: manual_note
title: Obsidian + Codex 个人 Wiki 配置记录
created_at: 2026-04-15
processing_status: processed

reviewed_at: 2026-04-15
processed_at: 2026-04-15
processed_into: [[wiki/sources/Obsidian-Codex-个人Wiki配置记录]]
tags:
  - obsidian
  - codex
  - wiki
---
# Obsidian + Codex 个人 Wiki 配置记录（简版）

## 目标

在 `nutrition-wiki` 中搭建一个可持续维护的个人知识库工作流：采集 raw -> 沉淀 wiki -> 审阅归档 -> 查询复用。

## 已完成配置

1. 克隆模板仓库 `obsidian-llm-wiki`。
2. 初始化本地库 `H:/inspool/nutrition-wiki`。
3. 写入基础结构：
   - `raw/unprocessed`
   - `raw/processed`
   - `raw/assets`
   - `wiki/sources`
   - `wiki/entities`
   - `wiki/concepts`
   - `wiki/synthesis`
4. 放入规则文件：
   - `AGENTS.md`
   - `CLAUDE.md`
5. 放入并修正 skills：
   - `.codex/skills/*`
   - 已同步到全局 `C:/Users/Administrator/.codex/skills/*`，可在面板中看到 `ingest_raw`、`query_wiki` 等。
6. 文案统一：
   - 将模板中的 `inspool-wiki-zh` 语境改为 `nutrition-wiki`。
7. 新增说明文档：
   - `README.md`（处理流程说明）
8. AGENTS 补充规则：
   - 操作 Obsidian 时优先使用 `obsidian-cli` skill。

## Web Clipper 关键配置

- Vault：`nutrition-wiki`
- 笔记位置：`raw/unprocessed`
- 注意：
  - 不要填绝对路径（如 `H:\...`）
  - 不要拼错目录名（`unprocessed`，不是 `unprecessed`）

## 推荐工作流（最小闭环）

1. 用 Web Clipper 把资料保存到 `raw/unprocessed`。
2. 执行 `$ingest_raw` 生成/更新 wiki 页面。
3. 人工审阅结果。
4. 执行 `$approve_ingest` 归档到 `raw/processed`。
5. 日常问答用 `$query_wiki`，高价值结论用 `$inspool` 回填。
6. 定期执行 `$lint_wiki` 做健康检查。

## 推荐插件（已讨论）

- Templater
- Dataview
- Another Quick Switcher
- Custom Attachment Location
- Outliner
- File Explorer Note Count

