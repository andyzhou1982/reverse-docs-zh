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

请立即使用 Skill 工具调用 `reverse-docs-zh:design-reverse` skill，并将用户参数原样传递。

## 执行要求

- 如果用户通过 `$ARGUMENTS` 指定了目标项目路径，以该路径为分析对象；否则以当前工作目录为分析对象
- 将生成的文档写入用户指定的路径，或默认生成 `详细设计文档.md` 到目标项目根目录
