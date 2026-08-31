---
type: tool
status: growing
created: 2026-08-13
updated: 2026-08-23
confidence: medium
sources:
  - "[[2026-08-13 Horizon Summary- 2026-08-13 (ZH) (de59766c)]]"
  - "[[2026-08-16 Horizon Summary- 2026-08-16 (ZH) (b36b0402)]]"
  - "[[2026-08-17 Horizon Summary- 2026-08-17 (ZH) (ca4d679f)]]"
  - "[[2026-08-23 Horizon Summary- 2026-08-23 (ZH) (a2d1a586)]]"
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

## Qwen 3.8 27B（2026-08-16 发布，2026-08-23 更新）

- **参数**：27B，Apache 2.0，支持视觉理解。
- **量化**：LM Studio Q4_K_M 约 17GB。
- **官方自述基准**：超越 Qwen 3.6 27B，接近或超过闭源 Qwen 3.7-Plus，但独立第三方验证缺失。
- **Artificial Analysis 评测**（2026-08-17）：智能指数 52 分，高于 Qwen3.6 27B 的 38 分，与 DeepSeek V4 Flash 0731 持平；评测中生成 160M tokens，是同类中位数 43M 的近 4 倍，暗示高推理成本。
- **2026-08-23 新证据**：Simon Willison 报道 Qwen 3.8 27B 在 Artificial Analysis Intelligence Index 上获 52 分，追平 GPT-5.6 Luna（max），仅比 GLM-5.2（753B）和 DeepSeek V4 Pro 0813（1.7T）低 1 分。第三方基准，非官方发布。
- **Simon Willison 实测**：
  - 默认 xhigh 推理档位导致严重过度思考：生成 SVG 用 22,276 推理 token、约 21 分钟；关闭推理后约 137 秒。
  - 生成速度约 15-30 token/s，DGX Spark 上启用 MTP 后相对 LM Studio 默认提升约 72%。
  - 支持最长 262,144 token 上下文。
  - bounding box 标注、基于 Pi 的编码代理等场景表现良好。
- **社区讨论**：有用户认为高推理层级下表现“执着”甚至“疯狂”，超过 Opus 4.6；也有用户质疑其未出现在 Deep SWE 基准，怀疑复杂任务速度慢。
- **推断**：默认推理档位设置可能损害用户体验，部署时应主动调整 reasoning_effort 并考虑 MTP 加速。
- **待验证**：官方基准的独立复现。

## 相关页面

- [[DeepSeek]]
- [[2026-08-13 AI 趋势综合]]
- [[2026-08-16 AI 趋势综合]]
- [[2026-08-17 AI 趋势综合]]
- [[2026-08-23 AI 趋势综合]]
- [[AI 博主内容系统]]
