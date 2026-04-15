---
type: concept
status: active
topic: Windows 文件创建入口配置
updated: 2026-04-14
supports:
  - "[[sources/右键新建添加md文档方法]]"
contradicts: []
related_entities:
  - "[[entities/Windows 注册表]]"
  - "[[entities/Typora]]"
related_concepts: []
related_sources:
  - "[[sources/右键新建添加md文档方法]]"
related_synthesis: []
---

# Windows 右键新建 Markdown 文档

## 定义

在 Windows 资源管理器中，通过注册表类型映射与 `ShellNew` 配置，让右键菜单支持直接新建 `.md` 文件。

## 核心机制

1. 为 `.md` 扩展名指定文件类型标识（示例为 `Typora.md`）。
2. 在 `HKEY_CLASSES_ROOT\.md\ShellNew` 下设置 `NullFile`，使系统可创建空白文件。
3. 通过导入 `.reg` 文件批量应用配置，并重启资源管理器使其生效。

见 [[sources/右键新建添加md文档方法#关键观点]]。

## 与相邻概念的区别

- 与“仅修改默认打开方式”不同，本概念关注的是“创建入口”，不是“打开行为”。
- 与“手工在注册表编辑器逐项修改”不同，本资料强调 `.reg` 导入流程。

## 支持证据

- [[sources/右键新建添加md文档方法]]

## 反例或限制

- 资料未提供跨版本验证，Windows 版本兼容性待确认。
- 依赖 `Typora.md` 类型是否已存在，待确认。

## 相关实体

- [[entities/Windows 注册表]]
- [[entities/Typora]]

## 相关来源

- [[sources/右键新建添加md文档方法]]
