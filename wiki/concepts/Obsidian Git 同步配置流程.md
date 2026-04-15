---
type: concept
status: draft
topic: obsidian-git-sync-workflow
updated: 2026-04-15
supports:
  - "[[sources/Obsidian-使用Git配置记录]]"
related_entities:
  - "[[entities/Obsidian]]"
  - "[[entities/Obsidian Git 插件]]"
  - "[[entities/GitHub]]"
related_sources:
  - "[[sources/Obsidian-使用Git配置记录]]"
---

# Obsidian Git 同步配置流程

## 定义

在 Obsidian 本地库中接入 Git 进行版本管理与跨设备同步的最小操作流程。

## 核心流程

1. 初始化并提交本地仓库。
2. 绑定远程仓库并完成认证。
3. 首次推送并建立跟踪分支。
4. 在 Obsidian Git 插件中配置自动提交/同步策略。

## 实践建议

- `Custom Git binary path` 默认留空，仅在系统 PATH 失效时填写绝对路径。
- 自动提交适合日常增量备份；关键改动建议手动 commit 并自定义消息。