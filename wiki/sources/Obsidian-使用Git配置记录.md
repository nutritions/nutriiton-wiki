---
type: source
status: draft
topic: obsidian-git-setup
updated: 2026-04-15
raw_note: "[[raw/unprocessed/2026-04-15-obsidian-git同步配置记录]]"
related_entities:
  - "[[entities/Obsidian]]"
  - "[[entities/Obsidian Git 插件]]"
  - "[[entities/GitHub]]"
related_concepts:
  - "[[concepts/Obsidian Git 同步配置流程]]"
related_sources:
  - "[[sources/Obsidian-Codex-个人Wiki配置记录]]"
---

# Obsidian 使用 Git 配置记录

## 来源信息

- 原始记录：[[raw/unprocessed/2026-04-15-obsidian-git同步配置记录]]
- 记录时间：2026-04-15

## 核心摘要

该记录给出从本地仓库初始化、绑定远程、完成认证到在 Obsidian Git 插件中设置自动提交模板的最小可用流程。

## 关键步骤

1. 本地初始化：`git init` -> `git add .` -> `git commit` -> `git branch -M main`。
2. 绑定远程：`git remote add origin ...`。
3. 认证后推送：`git push -u origin main`。
4. 在 Obsidian 启用 Obsidian Git 插件。
5. 插件配置：`Custom Git binary path` 默认留空；自动提交模板在 `Commit message on auto commit-and-sync` 设置。

## 关键观点

- 自动提交模板可提升历史可读性，例如：`wiki auto: {{date}} | {{numFiles}} files`。
- 如果希望每次手写提交说明，应关闭自动提交，改手动 commit。

## 待确认问题

- 自动提交频率与多设备同时编辑下冲突概率之间的平衡。