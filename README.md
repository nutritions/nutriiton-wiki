# Nutrition Wiki 使用说明

本仓库用于把零散资料持续沉淀为可检索、可演化的 Obsidian Wiki。

## 3 分钟上手

1. 把原始资料放到 `raw/unprocessed/`（Markdown 为主）。
2. 在对话中运行：`$ingest_raw`  
3. 审阅生成的 `wiki/` 页面，确认无误后运行：`$approve_ingest`
4. 日常问答运行：`$query_wiki`
5. 高价值问答回填运行：`$inspool`
6. 定期健康检查运行：`$lint_wiki`

## 文档处理标准流程

### 1. 采集（Capture）

- 入口目录：`raw/unprocessed/`
- 推荐内容：网页剪藏、文章、会议纪要、书摘、转写稿
- 原则：`raw/` 视为事实来源层，正文默认不改写

### 2. 入库沉淀（Ingest）

- 命令：`$ingest_raw`
- 主要动作：
  - 读取下一组待处理素材（一个 ingest 单元）
  - 在 `wiki/sources/` 创建或更新来源页
  - 同步更新 `wiki/entities/`、`wiki/concepts/`、`wiki/synthesis/`
  - 更新 `wiki/index.md`、`wiki/log.md`、`raw/index.md`
  - 将本批 raw 状态标记为 `pending_review`

### 3. 人工审阅（Review）

- 重点检查：
  - 命名是否清晰
  - 关键结论是否有来源支撑
  - 是否遗漏重要概念/实体
  - 是否存在过强结论或冲突未记录

### 4. 归档确认（Approve）

- 命令：`$approve_ingest`
- 触发条件：你确认本次 ingest 结果可接受
- 主要动作：
  - 将 `pending_review` 的 raw 迁移到 `raw/processed/`
  - 同步修复 wiki 中的 raw 路径引用
  - 记录到 `raw/index.md` 与 `wiki/log.md`

### 5. 知识查询（Query）

- 命令：`$query_wiki`
- 规则：优先基于 `wiki/` 已有页面回答，避免每次回到原始材料重做总结

### 6. 回填沉淀（Inspool）

- 命令：`$inspool`
- 场景：当一次问答有长期价值，回填为 `wiki/synthesis/` 页面

### 7. 巡检维护（Lint）

- 命令：`$lint_wiki`
- 检查项：孤立页面、弱证据结论、关系字段缺失、路径残留、索引不一致等

## 目录说明

- `raw/`：原始资料层（`unprocessed/`、`processed/`、`assets/`）
- `wiki/`：知识沉淀层（`sources/`、`entities/`、`concepts/`、`synthesis/`、`meta/`）
- `AGENTS.md`：Codex 执行规则入口
- `CLAUDE.md`：Claude 执行规则入口

## 常用对话指令示例

- `用 ingest_raw 处理 raw/unprocessed 的下一组资料`
- `运行 query_wiki：总结最近处理的主题脉络`
- `运行 approve_ingest，归档刚才那一批`
- `运行 lint_wiki，检查当前知识库健康度`

## 注意事项

- 未经确认，不要把 raw 从 `unprocessed` 直接移到 `processed`
- 关键结论尽量链接本地 `sources` 页面
- 不确定内容标注“待确认”，不要写成确定事实

