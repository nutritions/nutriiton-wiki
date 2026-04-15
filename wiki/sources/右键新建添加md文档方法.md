---
type: source
status: active
topic: Windows 右键新建 Markdown 文档
updated: 2026-04-14
raw_note: "[[raw/processed/others/右键新建添加md文档方法]]"
external_url: ""
related_entities:
  - "[[entities/Windows 注册表]]"
  - "[[entities/Typora]]"
related_concepts:
  - "[[concepts/Windows 右键新建 Markdown 文档]]"
related_sources: []
---

# 右键新建添加md文档方法

## 来源信息

- 原始资料：[[raw/processed/others/右键新建添加md文档方法]]
- 资料类型：操作笔记
- 主题：在 Windows 中恢复“右键新建 Markdown 文档”

## 核心摘要

该资料给出一套可执行流程：先创建包含注册表内容的文本文件，再改为 `.reg` 并导入，最后重启资源管理器以生效。文中指出“直接修改注册表的旧方法已失效”。

## 关键观点

1. 当前可行方案是通过 `.reg` 文件导入注册表，而不是沿用旧的“直接修改”路径。
2. `.md` 扩展名需映射到 `Typora.md`，并在 `ShellNew` 下设置 `NullFile`，用于在右键菜单中创建空白 Markdown 文件。
3. 若修改后未立即生效，需要重启 Windows 资源管理器。

## 证据摘录

- 注册表片段核心包含：`HKEY_CLASSES_ROOT\.md` 与 `HKEY_CLASSES_ROOT\.md\ShellNew`。
- 操作顺序明确为：创建文本文件 -> 写入注册表内容 -> 改后缀为 `.reg` -> 运行 -> 重启资源管理器。

## 可抽取实体

- [[entities/Windows 注册表]]
- [[entities/Typora]]

## 可抽取概念

- [[concepts/Windows 右键新建 Markdown 文档]]

## 与现有 wiki 的连接

- 该来源可作为 [[concepts/Windows 右键新建 Markdown 文档]] 的操作证据。
- 该来源为 [[entities/Windows 注册表]] 的实例性用法补充。

## 待确认问题

- “原直接修改注册表方法已失效”对应的具体 Windows 版本范围尚不明确，待确认。
- `Typora.md` 类型是否依赖本机 Typora 安装状态，待确认。

## 相关来源

- 暂无
