# Wiki 日志

本页用于记录正式的 ingest、approve、query、lint 与 refactor 时间线。

当前状态：

- 当前还没有正式处理记录
- 开源前测试数据已清理
- 后续可从第一篇 raw 素材开始重新积累时间线

## [2026-04-14] ingest | 右键新建添加md文档方法

- 处理 ingest 单元：`raw/processed/others/右键新建添加md文档方法.md`（已在 approve 后归档）
- 新增来源页：[[sources/右键新建添加md文档方法]]
- 新增概念页：[[concepts/Windows 右键新建 Markdown 文档]]
- 新增实体页：[[entities/Windows 注册表]]、[[entities/Typora]]
- 同步更新：[[index]] 与 `raw/index.md`
- 状态变更：该 raw 已标记为 `pending_review`，等待用户确认
- 待确认：方法的 Windows 版本兼容性、`Typora.md` 类型依赖条件

## [2026-04-14] approve | 右键新建添加md文档方法

- 归档 ingest 单元：已从待处理目录迁移到 `raw/processed/others/右键新建添加md文档方法.md`
- 流程字段更新：`processing_status: processed`，`reviewed_at: 2026-04-14`
- 已修复来源页 raw 引用到 `raw/processed/...`
- 局部自检：`wiki/` 下已无该文件对应的旧 `raw/unprocessed/...` 路径残留

## [2026-04-15] ingest | Codex+Obsidian 配置记录与代理配置

- 处理 ingest 单元：`raw/processed/others/codex-env-代理配置与作用说明.md` + `raw/processed/others/obsidian-codex-个人wiki配置记录.md`
- 新增来源页：[[sources/Codex-env-代理配置与作用说明]]、[[sources/Obsidian-Codex-个人Wiki配置记录]]
- 新增概念页：[[concepts/Codex 代理环境变量配置]]、[[concepts/Obsidian + Codex 个人Wiki工作流]]
- 新增实体页：[[entities/Codex]]、[[entities/Obsidian]]、[[entities/Obsidian Web Clipper]]、[[entities/代理服务]]
- 新增综合页：[[synthesis/Codex与Obsidian个人Wiki搭建要点]]
- 同步更新：[[index]] 与 `raw/index.md`
- 状态变更：本批 raw 已标记为 `pending_review`，等待用户确认后执行 approve
- 待确认：中文文件名在不同前端的链接跳转兼容性
## [2026-04-15] approve | Codex+Obsidian 配置记录与代理配置

- 归档 ingest 单元：`raw/processed/others/codex-env-代理配置与作用说明.md` + `raw/processed/others/obsidian-codex-个人wiki配置记录.md`
- 迁移结果：两篇 raw 已移动到 `raw/processed/`
- 流程字段更新：`processing_status: processed`，`reviewed_at: 2026-04-15`，`processed_at: 2026-04-15`
- 已修复来源页 raw 引用到 `raw/processed/...`
- 局部自检：`wiki/` 下已无本批文件对应的旧 `raw/unprocessed/...` 路径残留
## [2026-04-15] ingest | Obsidian Git 配置记录

- 处理 ingest 单元：`raw/processed/others/2026-04-15-obsidian-git同步配置记录.md`
- 新增来源页：[[sources/Obsidian-使用Git配置记录]]
- 新增概念页：[[concepts/Obsidian Git 同步配置流程]]
- 新增实体页：[[entities/Obsidian Git 插件]]、[[entities/GitHub]]
- 新增综合页：[[synthesis/Obsidian中Git配置最小闭环]]
- 同步更新：[[index]] 与 `raw/index.md`
- 状态变更：该 raw 已标记为 `pending_review`，等待用户确认
- 待确认：自动提交频率与多设备并发编辑下的冲突控制策略
## [2026-04-15] approve | Obsidian Git 配置记录

- 归档 ingest 单元：`raw/processed/others/2026-04-15-obsidian-git同步配置记录.md`
- 流程字段更新：`processing_status: processed`，`reviewed_at: 2026-04-15`，`processed_at: 2026-04-15`
- 已修复来源页 raw 引用到 `raw/processed/...`
- 局部自检：`wiki/` 下已无该文件对应的旧 `raw/unprocessed/...` 路径残留