---
type: source
status: draft
topic: codex-proxy-env
updated: 2026-04-15
raw_note: "[[raw/processed/codex-env-代理配置与作用说明]]"
related_entities:
  - "[[entities/Codex]]"
  - "[[entities/代理服务]]"
related_concepts:
  - "[[concepts/Codex 代理环境变量配置]]"
related_sources:
  - "[[sources/Obsidian-Codex-个人Wiki配置记录]]"
---

# Codex env 代理配置与作用说明

## 来源信息

- 原始记录：[[raw/processed/codex-env-代理配置与作用说明]]
- 记录时间：2026-04-15

## 核心摘要

该记录总结了在 Codex 场景下通过 `.env` 与启动脚本配置代理的实践要点：环境变量覆盖、端口就绪检测、进程重启与稳定性验证。

## 关键观点

- 代理变量需要覆盖 HTTP/HTTPS 与 WebSocket，并兼容大小写读取差异。
- `NO_PROXY` 应包含本地回环地址，避免本地服务误走代理。
- 对不会自动读取 `.env` 的应用，需要通过启动脚本显式注入变量。

## 证据摘录

- 环境变量示例：`HTTP_PROXY / HTTPS_PROXY / ALL_PROXY / WS_PROXY / WSS_PROXY`。
- 启动脚本流程：检测 `127.0.0.1:7897` -> 关闭旧进程 -> 注入变量后重启。

## 待确认问题

- 不同网络环境下，WebSocket 重连问题是否完全由代理链路导致。
- Codex 桌面端对 `.env` 自动加载边界是否在后续版本变化。