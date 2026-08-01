---
type: tool
status: growing
created: 2026-08-01
updated: 2026-08-01
confidence: medium
sources:
  - "[[2026-08-01 Horizon Summary- 2026-08-01 (ZH) (c5dcc0d9)]]"
tags:
  - mcp
  - agents
  - protocol
---

# MCP（Model Context Protocol）

## 概述

MCP 是 Anthropic 提出的开放协议，用于标准化 AI 模型与外部工具、数据源的交互。

## MCP 2.0（无状态）

- **发布日期**：2026-07-28
- **核心变化**：从需要 initialize 获取 session ID 的两步流程，改为单 HTTP 请求 + 头部（MCP-Protocol-Version、Mcp-Method）完成工具调用。
- **优点**：简化客户端和服务端实现，便于 Web 部署和横向扩展。

## Simon Willison 的工具

- **mcp-explorer**：交互式探测 MCP 服务器的 CLI。
- **datasette-mcp**：为 Datasette 添加 MCP 端点，提供只读工具。
- **llm-mcp-client**：LLM 工具的 MCP 客户端 alpha 插件。

## 安全观点

Simon 认为 MCP 工具比直接给 agent shell/curl 权限更易审计和控制，但这是个人观点，需结合场景验证。

## 相关页面

- [[AI 博主内容系统]]
- [[LLM Wiki]]
