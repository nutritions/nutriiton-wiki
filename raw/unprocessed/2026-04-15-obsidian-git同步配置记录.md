---
source_type: conversation_note
title: Obsidian Git 同步配置过程记录
created_at: 2026-04-15
processing_status: unprocessed
tags:
  - obsidian
  - git
  - sync
  - plugin
---

# Obsidian Git 同步配置过程记录

## 记录时间

2026-04-15

## 来源说明

来自本次会话中关于 Obsidian 多设备同步与 Git 插件配置的讨论。

## 原始要点

1. 多设备同步可用三种方案：Obsidian Sync（付费）、云盘同步、Git 同步。
2. 最终选用 Git 方案，并在本地仓库 `H:\inspool\nutrition-wiki` 完成初始化与首个提交。
3. 远程仓库地址已确认：`https://github.com/nutritions/nutriiton-wiki.git`。
4. 推送时若出现 GitHub 认证问题，可使用 `gh auth login`；若 `gh` 不存在，先安装 GitHub CLI。
5. 认证报网络超时时，可改为 `--with-token` 方式进行 PAT 登录。
6. Obsidian Git 插件中的 `Custom Git binary path` 一般留空即可；只有无法识别 git 时才填完整路径。
7. 自动提交信息模板位置是 `Commit message on auto commit-and-sync`。
8. 模板示例 `wiki auto: {{date}} | {{numFiles}} files` 的实际效果类似：`wiki auto: 2026-04-15 10:32:18 | 7 files`。
9. 若希望每次手写提交说明，应关闭自动提交并改为手动 commit。

## 待后续 ingest 提示

- 可沉淀为来源页：Obsidian Git 插件最小可用配置。
- 可抽取概念：自动提交模板、PAT 登录、跨设备同步策略对比。