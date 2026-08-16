---
type: concept
status: seed
created: 2026-08-12
updated: 2026-08-12
confidence: low
sources:
  - "[[2026-08-12 Horizon Summary- 2026-08-12 (ZH) (eac950a7)]]"
tags:
  - moe
  - llm
  - korea
  - gdla
---

# Motif 3

## 定义

Motif 3 是一个由 Motif Technologies 发布的 decoder-only 混合专家（MoE）语言模型，总参数量 314B，每个 token 激活 13.2B 参数。

## 技术特点

- **架构**：每层稀疏 MoE 有 384 个路由专家，每次选取 8 个专家；采用 Grouped Differential Latent Attention（GDLA）架构，结合多 token 预测、专家特定 PolyNorm 激活与流形约束超连接。
- **预训练**：约 12.5 万亿 token，覆盖网页、STEM、代码、数学、多语言等领域，训练上下文最长 256K。
- **后训练**：融合通用 SFT、6 个强化学习训练的专家教师以及 1 个软件工程 SFT 教师，通过多教师在线策略蒸馏合并能力。

## 发布信息

- **技术报告**：arXiv:2608.09119（2026-08-11 预印本）。
- **定位**：面向韩国 AI 模型竞争背景，与 Upstage、LG AI Research、SKT 等厂商形成对比。

## 事实与推断

- **事实**：报告称其在推理、代码、长上下文和智能体任务上达到领先开源模型水平。
- **推断**：稀疏激活架构与 256K 上下文训练能力意味着推理成本和长文本处理是大模型落地中值得验证的方向。
- **待验证**：预印本，基准表现需独立验证；权重开放情况未明确。

## 相关页面

- [[2026-08-12 AI 趋势综合]]
- [[vLLM]]
- [[DeepSeek]]
