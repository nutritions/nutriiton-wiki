---
type: entity
status: active
topic: Markdown 编辑器
updated: 2026-04-14
supports:
  - "[[sources/右键新建添加md文档方法]]"
contradicts: []
related_entities:
  - "[[entities/Windows 注册表]]"
related_concepts:
  - "[[concepts/Windows 右键新建 Markdown 文档]]"
related_sources:
  - "[[sources/右键新建添加md文档方法]]"
related_synthesis: []
---

# Typora

## 一句话定义

Typora 是一款 Markdown 编辑器，在本来源中作为 `.md` 文件类型标识 `Typora.md` 的关联对象出现。

## 背景

来源资料中通过将 `.md` 映射到 `Typora.md`，配合 `ShellNew` 的 `NullFile` 实现右键新建 Markdown 文件。见 [[sources/右键新建添加md文档方法#关键观点]]。

## 关键属性

- 作为文件类型标识关联目标出现。
- 与 Windows 注册表配置联动影响右键新建菜单行为。

## 支持证据

- [[sources/右键新建添加md文档方法]]

## 分歧与冲突

- 当前资料未确认 `Typora.md` 在未安装 Typora 环境下是否可稳定使用，待确认。

## 相关事件或观点

- 在该操作方法中，`Typora.md` 用于承接 `.md` 扩展名映射。

## 相关概念

- [[concepts/Windows 右键新建 Markdown 文档]]

## 相关来源

- [[sources/右键新建添加md文档方法]]

## 未决问题

- 该映射是否必须由 Typora 安装过程预先注册，待补充证据。
