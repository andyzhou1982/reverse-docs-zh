# 各语言代码探索策略

根据阶段零识别的技术栈，选择对应的章节进行代码探索。

## Java 项目

- API 层：`find` 列出 `*Controller.java`、`*Api.java`（Feign 接口）
- 数据层：`find` 列出 `*/domain/po/*` 或 `*/entity/*` 实体类
- 外部调用：`find` 列出 `*/external/client/*`（Feign 客户端）、`*Producer.java`（MQ 生产者）
- 定时任务：`find` 列出 `*Job.java`、`*Task.java`、`*Scheduler.java`
- 安全配置：查找 `ResourceServerConfiguration`、`SecurityConfig` 等安全相关类

## Python 项目

- API 层：`find` 列出 `*views.py`、`*api.py`、`*router.py`、`*endpoint.py`、`*resource.py`
- 数据层：`find` 列出 `*models.py`、`*schema.py`、`*entity.py`，或 ORM 模型目录
- 外部调用：`find` 列出 `*client.py`、`*service.py`、查找 HTTP 调用（requests/httpx/aiohttp）
- 异步任务：`find` 列出 `*task.py`、`*celery.py`、`*job.py`
- 配置：查找 `settings.py`、`config.py`、`.env`、`alembic.ini`（数据库迁移）

## Go 项目

- API 层：`find` 列出 `*handler.go`、`*controller.go`、`*router.go`、`*server.go`
- 数据层：`find` 列出 `*model.go`、`*entity.go`、`*repository.go`、`*store.go`
- 外部调用：`find` 列出 `*client.go`、`*grpc.go`，查找 RPC/HTTP 调用
- 后台任务：`find` 列出 `*cron.go`、`*worker.go`、`*job.go`
- 配置：查找 `config.yaml`、`*.toml`、config 结构体定义

## Node.js / 前端项目

- API 层：`find` 列出 `*route*`、`*controller*`、`*api*`、`*handler*`
- 数据层：`find` 列出 `*model*`、`*schema*`、`prisma/schema.prisma`、`*entity*`
- 外部调用：`find` 列出 `*client*`、`*service*`、查找 axios/fetch/gRPC 调用
- 前端页面：列出 `views/`、`pages/`、`components/` 目录结构
- 前端 API 模块：列出 `api/`、`services/` 目录
- 配置：查找 `webpack.config.*`、`vite.config.*`、`next.config.*`、`tsconfig.json`
