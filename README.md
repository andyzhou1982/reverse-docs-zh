# reverse-docs-zh

从源代码逆向生成中文详细设计文档的 Claude Code 插件。

## 功能

- 支持多语言项目：Java、Python、Go、Node.js 等
- GitNexus 知识图谱优先，自动降级到内置工具分析
- 基于模板的文档生成，包含架构图、时序图、数据设计等
- 严格防伪造：所有内容来自实际代码分析

## 安装

### 方式一：通过市场安装（推荐）

在 Claude Code 会话内执行：

```
/plugin marketplace add andyzhou1982/reverse-docs-zh
```

添加市场后，安装插件：

```
/plugin install reverse-docs-zh@reverse-docs-zh-marketplace
```

也可在外部终端中执行：

```bash
claude plugin marketplace add andyzhou1982/reverse-docs-zh
```

### 方式二：本地插件目录

```bash
claude --plugin-dir /path/to/reverse-docs-zh
```

## 使用

```
/reverse-docs-zh:design-reverse [目标项目路径或描述]
```

不指定路径时，默认分析当前工作目录的代码库。

### 示例

```
# 分析当前目录的代码库
/reverse-docs-zh:design-reverse

# 分析指定路径的项目
/reverse-docs-zh:design-reverse /path/to/my-project

# 附带描述信息
/reverse-docs-zh:design-reverse 这是一个 Spring Boot 微服务项目
```

### 生成内容

插件会根据代码分析自动生成以下章节（信息充足时）：

- 系统架构设计（含 Mermaid 架构图）
- 模块详细设计（含时序图、状态图）
- 数据设计（ER 图、表结构）
- 接口设计（外部 API、模块间调用）
- 非功能性设计（安全、性能、可观测性）

## 组件

| 组件 | 说明 |
|------|------|
| `skills/design-reverse` | 核心逆向生成 skill |
| `commands/design-reverse` | 用户触发的斜杠命令 |
| `references/detailed-design-template.md` | 详细设计文档模板 |
| `references/language-exploration-guide.md` | 各语言代码探索策略 |

## 仓库

https://github.com/andyzhou1982/reverse-docs-zh

## 作者

andyz
