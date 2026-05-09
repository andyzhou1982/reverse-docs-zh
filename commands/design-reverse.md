---
description: 从源代码逆向生成中文详细设计文档
argument-hint: "[目标项目路径或描述]"
allowed-tools:
  - Read
  - Grep
  - Glob
  - Bash
  - Agent
  - Write
  - Edit
  - AskUserQuestion
  - WebSearch
  - mcp__web_reader__webReader
  - TaskCreate
  - TaskUpdate
  - TaskList
  - TaskGet
  - NotebookEdit
---

# 从代码逆向生成详细设计文档

请执行 design-reverse skill 中定义的完整工作流，从现有代码库逆向生成完整的项目详细设计文档。

## 执行要求

- 如果用户通过 `$ARGUMENTS` 指定了目标项目路径，以该路径为分析对象；否则以当前工作目录为分析对象
- 严格按照 skill 中定义的五阶段工作流执行（收集模板与项目概况 → 深入探索各模块 → 交叉验证与补充 → 生成文档 → 自检）
- 将生成的文档写入用户指定的路径，或默认生成 `详细设计文档.md` 到目标项目根目录
