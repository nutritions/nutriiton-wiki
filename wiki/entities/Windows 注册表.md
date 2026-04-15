---
type: entity
status: active
topic: Windows 系统配置组件
updated: 2026-04-14
supports:
  - "[[sources/右键新建添加md文档方法]]"
contradicts: []
related_entities:
  - "[[entities/Typora]]"
related_concepts:
  - "[[concepts/Windows 右键新建 Markdown 文档]]"
related_sources:
  - "[[sources/右键新建添加md文档方法]]"
related_synthesis: []
---

# Windows 注册表

## 一句话定义

Windows 注册表是系统与应用配置的层级数据库，可通过键值控制文件类型与系统行为。

## 背景

在“右键新建 Markdown 文档”场景中，注册表用于定义 `.md` 扩展名的类型映射和新建入口。见 [[sources/右键新建添加md文档方法#证据摘录]]。

## 关键属性

- 路径层级明确，支持按键组织配置。
- 可通过 `.reg` 文件导入批量配置。
- 配置变更后可能需要重启资源管理器才能立即生效。

## 支持证据

- [[sources/右键新建添加md文档方法]]

## 分歧与冲突

- 关于“直接修改注册表旧方法失效”的版本边界尚不清晰，待确认。

## 相关事件或观点

- 通过 `HKEY_CLASSES_ROOT\.md` 与 `HKEY_CLASSES_ROOT\.md\ShellNew` 配置可启用右键新建 `.md`。

## 相关概念

- [[concepts/Windows 右键新建 Markdown 文档]]

## 相关来源

- [[sources/右键新建添加md文档方法]]

## 未决问题

- 该方法在不同 Windows 版本上的稳定性差异有待补证。
