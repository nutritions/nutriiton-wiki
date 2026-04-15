---
source_type: manual_note
title: Codex .env 代理配置与作用说明
created_at: 2026-04-15
processing_status: processed
processed_into: [[wiki/sources/Codex-env-代理配置与作用说明]]

reviewed_at: 2026-04-15
processed_at: 2026-04-15
tags:
  - codex
  - proxy
  - env
---

# Codex `.env` 代理配置与作用说明

## 配置位置

本次将代理配置写入：

- `C:\Users\Administrator\.codex\.env`

## 配置内容（示例）

```env
HTTP_PROXY=http://127.0.0.1:7897
HTTPS_PROXY=http://127.0.0.1:7897
ALL_PROXY=http://127.0.0.1:7897
WS_PROXY=http://127.0.0.1:7897
WSS_PROXY=http://127.0.0.1:7897
http_proxy=http://127.0.0.1:7897
https_proxy=http://127.0.0.1:7897
all_proxy=http://127.0.0.1:7897
NO_PROXY=localhost,127.0.0.1,::1
no_proxy=localhost,127.0.0.1,::1
```

## 这样设置的作用

1. 统一声明 HTTP、HTTPS 与 WebSocket 的代理出口。
2. 兼容不同程序对环境变量大小写的读取差异。
3. 通过 `NO_PROXY` 避免本地环回地址走代理，减少本地服务互访异常。
4. 为需要环境变量代理的命令行工具和部分应用提供默认代理上下文。

## 生效边界

- `.env` 文件是否生效，取决于目标程序是否会主动读取该 `.env`。
- 对不会自动读取 `.env` 的桌面应用，通常需要通过启动脚本显式注入环境变量。
- 已在运行中的进程通常不会自动重载新环境变量，需重启对应应用。

## 配套启动脚本（已实践）

为了提高稳定性，使用批处理脚本执行以下流程：

1. 先检测 `127.0.0.1:7897` 代理端口是否就绪。
2. 关闭旧的 `Codex.exe` / `Code.exe` 进程。
3. 在同一进程上下文下设置代理环境变量后重启应用。

该方案可减少“首次对话反复重连”的概率，但不能替代代理节点本身稳定性。

## 简单验证方法

1. 启动代理软件，确认 `7897` 在监听。
2. 通过脚本启动 Codex。
3. 新开多个会话观察是否仍频繁重连。
4. 若仍不稳定，优先排查代理规则、节点质量和 WebSocket 转发链路。
