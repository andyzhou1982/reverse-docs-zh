# reverse-docs-zh

从源代码逆向生成中文详细设计文档的 Claude Code 插件。

## 功能

- 支持多语言项目：Java、Python、Go、Node.js 等
- GitNexus 知识图谱优先，自动降级到内置工具分析
- 基于模板的文档生成，包含架构图、时序图、数据设计等
- 严格防伪造：所有内容来自实际代码分析

## 安装

```bash
claude --plugin-dir /path/to/reverse-docs-zh
```

## 使用

```
/reverse-docs-zh:design-reverse [目标项目路径或描述]
```

不指定路径时，默认分析当前工作目录的代码库。

## 组件

| 组件 | 说明 |
|------|------|
| `skills/design-reverse` | 核心逆向生成 skill |
| `commands/design-reverse` | 用户触发的斜杠命令 |
| `skills/design-reverse/references/detailed-design-template.md` | 详细设计文档模板 |
| `skills/design-reverse/references/language-exploration-guide.md` | 各语言代码探索策略 |

## 作者

andyz
