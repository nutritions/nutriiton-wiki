# Raw 索引

本页用于记录 `nutrition-wiki/raw/` 的处理队列与已处理记录。

这是流程视图，不是内容索引。内容导航请看 `nutrition-wiki/wiki/index.md`。

说明：默认处理单位不是固定“一篇”，而是一个 ingest 单元。该单元可以是单篇文件，也可以是一组明确相关的文件。

## 队列概览

- 未处理：0
- 待确认：0
- 已处理：4
- 最新完成：2026-04-15（approve）

## 未处理素材

- 暂无

## 待确认素材

- 暂无

## 已处理素材

- `raw/processed/右键新建添加md文档方法.md` -> `wiki/sources/右键新建添加md文档方法.md`（processed_at: 2026-04-14, reviewed_at: 2026-04-14）
- `raw/processed/codex-env-代理配置与作用说明.md` -> `wiki/sources/Codex-env-代理配置与作用说明.md`（processed_at: 2026-04-15, reviewed_at: 2026-04-15）
- `raw/processed/obsidian-codex-个人wiki配置记录.md` -> `wiki/sources/Obsidian-Codex-个人Wiki配置记录.md`（processed_at: 2026-04-15, reviewed_at: 2026-04-15）
- `raw/processed/2026-04-15-obsidian-git同步配置记录.md` -> `wiki/sources/Obsidian-使用Git配置记录.md`（processed_at: 2026-04-15, reviewed_at: 2026-04-15）

## 维护规则

- 新素材进入 `unprocessed/`
- 每次 ingest 默认只处理一个 ingest 单元
- ingest 成功后先标记为 `pending_review`
- 只有用户确认后，才迁移到 `processed/`
- 如果 raw 文件正文未动，只更新了流程元数据，这仍然视为原始资料层