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

用户通过 `/reverse-docs-zh:design-reverse` 调用此命令，从现有代码库逆向生成完整的项目详细设计文档。

## 执行步骤

1. **加载核心 Skill**: 读取并遵循 `skills/design-reverse/SKILL.md` 中定义的完整工作流
2. **确定目标**: 如果用户通过 `[目标项目路径或描述]` 指定了目标项目，以指定路径为分析对象；否则以当前工作目录为分析对象
3. **按照 Skill 的五阶段工作流执行**:
   - 阶段一：收集模板与项目概况
   - 阶段二：深入探索各模块
   - 阶段三：交叉验证与补充
   - 阶段四：生成文档
   - 阶段五：自检
4. **输出**: 将生成的文档写入用户指定的路径，或默认生成 `详细设计文档.md` 到目标项目根目录

## 重要约束

- 必须先读取 `skills/design-reverse/references/detailed-design-template.md` 模板文件，严格按照模板章节结构生成文档
- 所有内容必须来自代码分析，绝不编造
- 使用中文编写文档，技术术语保留英文
- 优先使用 GitNexus（如可用），否则降级到内置工具
