---
source_type: conversation_note
title: Obsidian 使用 Git 配置记录
created_at: 2026-04-15
processing_status: processed
processed_into: [[wiki/sources/Obsidian-使用Git配置记录]]

reviewed_at: 2026-04-15
processed_at: 2026-04-15
tags:
  - obsidian
  - git
---

# Obsidian 使用 Git 配置记录

## 记录时间

2026-04-15

## 来源说明

来自本次会话中关于在 Obsidian 中配置 Git 的实操过程。

## 配置步骤

1. 在本地库初始化 Git：
   - `git init`
   - `git add .`
   - `git commit -m "init nutrition-wiki"`
   - `git branch -M main`
2. 绑定远程仓库：
   - `git remote add origin https://github.com/nutritions/nutriiton-wiki.git`
3. 完成 GitHub 认证后推送：
   - `git push -u origin main`
4. 在 Obsidian 安装并启用 `Obsidian Git` 插件。
5. 插件设置要点：
   - `Custom Git binary path` 默认留空（仅识别不到 git 时再填完整路径）。
   - 自动提交模板在 `Commit message on auto commit-and-sync` 中设置。
   - 模板示例：`wiki auto: {{date}} | {{numFiles}} files`。
6. 如果希望每次手写提交说明：关闭自动提交，改用手动 commit。

## 待后续 ingest 提示

- 可沉淀为来源页：Obsidian Git 插件最小可用配置。