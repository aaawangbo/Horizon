---
type: tool
status: growing
created: 2026-08-15
updated: 2026-08-23
confidence: medium
sources:
  - "[[2026-08-13 Horizon Summary- 2026-08-13 (ZH) (de59766c)]]"
  - "[[2026-08-14 Horizon Summary- 2026-08-14 (ZH) (b27a4e10)]]"
  - "[[2026-08-23 Horizon Summary- 2026-08-23 (ZH) (a2d1a586)]]"
tags:
  - llm
  - chinese-llm
  - zhipu-ai
---

# GLM

## 定义

GLM（General Language Model）是智谱 AI（Zhipu AI）开发的大语言模型系列，涵盖 ChatGLM、GLM-4 及 GLM-5 等代际产品。该系列在国内开源生态中具有较高影响力，常被作为低成本 API 或本地部署选项与 DeepSeek、Kimi、MiniMax 等模型进行性价比对比。

## 近期动态

- **GLM-5.2**（2026-08 社区提及）：在 OpenRouter 等平台上作为低成本模型被开发者用于代码、推理等任务，与 Kimi-K3、MiniMax 等在价格性能比上进行竞争。具体基准数据需独立验证。
- **GLM-5.3 发布**（2026-08-14）：Z.ai 官方博客宣称具备前沿编码能力和新兴网络能力（cyber capabilities）。社区用户称通过 Claude Code 接入后可完成安全研究任务（如 WordPress 插件 0-day、RCE、内核漏洞利用），并提及订阅费用从 $18 升至 $80。另有评论指出 z.ai 正在批量扫描开源软件并披露 CVE。
- **GLM-5.3 破解 Fire 平板**（2026-08-23）：作者自述花费 266 美元，用四个 AI 模型尝试 Root 亚马逊 Fire 平板，GLM-5.3 一天内通过发现未修补漏洞并编写利用代码完成 Root；美国模型因安全机制拒绝协助。单次自述，无复现细节。

## 注意事项

- GLM 系列不同版本的开放程度不一，部分版本提供开源权重，部分仅通过 API 提供。
- 社区对比多为个人使用偏好，缺乏系统化基准测试，需谨慎参考。
- GLM-5.3 的官方基准和独立复现尚未公开，需谨慎看待其评估口径。

## 相关页面

- [[LLM Wiki]]
- [[2026-08-14 AI 趋势综合]]
- [[2026-08-23 AI 趋势综合]]
- [[AI 安全事件]]
