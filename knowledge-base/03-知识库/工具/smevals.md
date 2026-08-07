---
type: tool
status: growing
created: 2026-08-01
updated: 2026-08-06
confidence: medium
sources:
  - "[[2026-08-01 Horizon Summary- 2026-08-01 (ZH) (c5dcc0d9)]]"
  - "[[2026-08-05 Horizon Summary- 2026-08-05 (ZH) (83ac2948)]]"
tags:
  - evals
  - llm
  - open-source
  - benchmarks
---

# smevals

## 概述

smevals 是 Simon Willison 与 Prime Radiant 合作开源的轻量 LLM 评测工具，用于对模型、提示词和 agent 框架运行小型评测并打分。

## 使用

- 安装：`uvx smevals`
- 运行评测：`uvx smevals run path-to-eval/ -m gpt-5.5 -m claude-opus-4.6`
- 评分和展示：`grade`、`serve`、`build` 命令
- 评测定义：目录 + YAML 文件

## 核心概念

eval、task、config、run、runner、grader、grade、check、checker。

## 相关基准与框架

### ParamBench（2026-08-05 预印本）
- **定位**：面向工具调用参数生成的难度分级基准，数据来自真实云网络 API。
- **方法**：probe-guided 框架（PBT/PGR），利用线性探针判断参数正确性。
- **结果**：5 个开源模型平均精确匹配率从 19.7% 提升到 59.6%。
- **注意**：预印本，领域单一，泛化性待验证。

### 可达性审计框架（2026-08-05 预印本）
- **核心**：区分“已实现”与“可达”能力，基准分数提升可能只是能力更稳定。
- **案例**：DAPO 部署分数上升 14.7 分，可达上限下降 13.3 分。
- **建议**：模型报告应同时披露两个指标。

## 定位

适合小团队和个人项目快速比较模型能力，但大规模基准和复杂评分标准支持有限。

## 相关页面
- [[AI 博主内容系统]]
- [[LLM Wiki]]
- [[2026-08-05 AI 趋势综合]]
