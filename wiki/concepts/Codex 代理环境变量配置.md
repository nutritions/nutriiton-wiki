---
type: concept
status: draft
topic: codex-proxy
updated: 2026-04-15
supports:
  - "[[sources/Codex-env-代理配置与作用说明]]"
related_entities:
  - "[[entities/Codex]]"
  - "[[entities/代理服务]]"
related_sources:
  - "[[sources/Codex-env-代理配置与作用说明]]"
---

# Codex 代理环境变量配置

## 定义

在 Codex 使用场景中，通过环境变量声明网络代理出口，并通过脚本控制启动时机与生效边界。

## 核心机制

- 配置多协议变量（HTTP/HTTPS/WS/WSS）。
- 用 `NO_PROXY` 保留本地地址直连。
- 通过启动脚本确保变量在目标进程启动前注入。

## 限制

- 仅写 `.env` 不保证所有应用自动加载。
- 代理节点不稳定时，配置正确也会出现重连。