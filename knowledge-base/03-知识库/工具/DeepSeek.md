---
type: tool
status: growing
created: 2026-08-01
updated: 2026-08-13
confidence: medium
sources:
  - "[[2026-08-01 Horizon Summary- 2026-08-01 (ZH) (c5dcc0d9)]]"
  - "[[2026-08-02 Horizon Summary- 2026-08-02 (ZH) (b0564d1c)]]"
  - "[[2026-08-01 Horizon Summary- 2026-08-01 (ZH) (20f3ca65)]]"
  - "[[2026-08-06 Horizon Summary- 2026-08-06 (ZH) (98b7a219)]]"
  - "[[2026-08-14 Horizon Summary- 2026-08-14 (ZH) (af99a363)]]"
  - "[[2026-08-13 Horizon Summary- 2026-08-13 (ZH) (de59766c)]]"
tags:
  - deepseek
  - llm
  - open-source
  - agent-framework
---

# DeepSeek

## 概述

DeepSeek 是中国 AI 公司，以开源模型和低成本 API 著称。

## 最新发布

### DeepSeek V4 Flash 0731（2026-07-31）

- **参数**：304B
- **权重大小**：约 167GB
- **API 价格**：输入 $0.14/M token，输出 $0.27/M token
- **特点**：据 Simon Willison 转述，智能体能力增强；第三方排名（Artificial Analysis）显示智能指数超过 MiniMax M3（428B）。
- **注意**：官方公告未直接提供，信息来自博客和第三方图表。
- **实测**：Simon 实测默认推理档位下生成“骑自行车的鹈鹕”图效果不佳，调高 reasoning_effort 后改善。

### DeepSeek V4 Pro 0813（2026-08-12 发布）

- **参数**：1.7T 总参数（此前资料称 1.6T，需核实），约 893GB 权重。
- **开源**：Hugging Face 上放出开源权重，API 已上线 OpenRouter 等渠道。
- **OpenRouter 上线**（2026-08-12）：API-only 形式出现，定价输入 $0.435/M token、输出 $0.87/M token，上下文长度 104 万 token，最大输出 38.4 万 token。无官方公告页面，信息来自 OpenRouter 与第三方基准。
- **社区实测**：有开发者称用于流量模拟/物理引擎任务约花费 $12.50 处理 2B（50% 缓存命中）获得明显改进；Simon Willison 测试渲染器时发现小篮子未出现在正确位置。
- **注意**：官方基准尚未发布，网上流传的基准表来自非正式渠道（微信群、Reddit 已删帖、HN 转贴），可信度待验证。

### DeepSeek Harness（2026-08-13 预览）

- **定位**：AI Agent 开发框架，核心特点是完整可追溯性：模型看到的所有内容（系统提示词、推理过程、工具调用及结果、子代理调度、上下文注入）写入只追加会话日志，可在 Trajectory 视图按来源检查，支持恢复、分叉、搜索和回放。
- **开源**：MIT 许可证，GitHub 仓库 deepseek-ai/deepseek-harness。
- **状态**：早期开发者预览版，作者确认会有破坏性变更。
- **相关**：核心之一是 Cordis v4 插件系统，支持热加载/卸载并还原状态和副作用。

## 相关页面

- [[LLM Wiki]]
- [[AI 博主内容系统]]
- [[2026-08-01 AI 趋势综合]]
- [[2026-08-06 AI 趋势综合]]
- [[2026-08-14 AI 趋势综合]]
- [[2026-08-13 AI 趋势综合]]
