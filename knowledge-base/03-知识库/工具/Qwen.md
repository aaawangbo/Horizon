---
type: tool
status: seed
created: 2026-08-13
updated: 2026-08-13
confidence: medium
sources:
  - "[[2026-08-13 Horizon Summary- 2026-08-13 (ZH) (de59766c)]]"
tags:
  - qwen
  - llm
  - open-source
  - moe
---

# Qwen

## 概述

Qwen 是阿里巴巴通义千问团队开发的大语言模型系列，涵盖不同规模与定位的模型变体。

## Qwen3.8-2.4T-A95B（2026-08-12 发布）

- **参数**：总参 2.4T，激活约 95B（MoE）。
- **权重**：Hugging Face 提供 BF16 与 FP8 权重。
- **社区转述性能**：介于 Opus 4.8 与 Fable 5 之间，被视为 Kimi K3 直接竞品。
- **注意**：默认无视觉输入、1M 上下文、内置工具等 Qwen3.8-Max 增强功能。
- **许可**：内网或年收入低于 5000 万美元可免费商用，超出后用于服务或商业化有额外限制。
- **部署**：BF16 原版约 4.9TB，社区提到 1bit 量化约 397GB。发布时无 QAT q4 权重，启动阶段比 Kimi K3 更难服务。
- **待验证**：官方完整评测和第三方独立验证尚未充分公开。

## 相关页面

- [[DeepSeek]]
- [[2026-08-13 AI 趋势综合]]
- [[AI 博主内容系统]]
