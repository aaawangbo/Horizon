---
type: tool
status: seed
created: 2026-08-01
updated: 2026-08-01
confidence: medium
sources:
  - "[[2026-08-01 Horizon Summary- 2026-08-01 (ZH) (c5dcc0d9)]]"
tags:
  - evals
  - llm
  - open-source
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

## 定位

适合小团队和个人项目快速比较模型能力，但大规模基准和复杂评分标准支持有限。

## 相关页面

- [[AI 博主内容系统]]
- [[LLM Wiki]]
