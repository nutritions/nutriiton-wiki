---
name: capture-to-unprocessed
description: 将用户在对话中给出的有用信息快速落盘为 raw/unprocessed 下的原始记录。适用于跨工作区交流后需要先记下来再 ingest 的场景；当用户说写进 wiki、记到 unprocessed、先存原始记录时使用。
---

# capture-to-unprocessed

将用户口述内容整理为一条新的 raw 记录，并写入 `raw/unprocessed/`。

## 执行步骤

1. 优先使用用户明确给出的目标目录或文件名。
2. 如果用户未给出路径，按以下优先级选择目标目录：
   - 当前工作区下的 `nutrition-wiki/raw/unprocessed/`
   - 当前工作区下任意 `*/raw/unprocessed/`
3. 如果找到多个候选目录，优先选择路径最短且名称最贴近 `nutrition-wiki` 的目录；无法判断时，先说明将使用的目录并继续执行。
4. 将用户提供的信息整理成原始记录风格，避免过度总结，保留上下文事实。
5. 文件命名优先使用 `YYYY-MM-DD-主题关键词.md`；若主题不明确，使用 `YYYY-MM-DD-会话记录.md`。
6. 以 UTF-8（无 BOM）写入文件。
7. 写入后返回：实际写入路径、文件名、记录摘要（1-3 行）。

## 记录模板

建议结构：标题、记录时间、来源说明、原始要点、待后续 ingest 提示（可选）。

## 约束

- 不要把未提供的信息补写成事实。
- 不要直接改写 `wiki/` 页面；本 skill 只负责落到 `raw/unprocessed/`。
- 如果目标目录不存在，先创建目录再写入。
