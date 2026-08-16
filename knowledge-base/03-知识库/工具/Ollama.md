---
type: tool
status: seed
created: 2026-08-15
updated: 2026-08-16
confidence: high
sources:
  - "[[2026-08-05 Horizon Summary- 2026-08-05 (ZH) (83ac2948)]]"
  - "[[2026-08-11 Horizon Summary- 2026-08-11 (ZH) (b6971f89)]]"
tags:
  - llm
  - local-inference
  - open-source
  - tool
---

# Ollama

## 定义

Ollama 是一个开源的本地大模型运行工具，提供简洁的 CLI 和 API 来下载、管理和运行各类 LLM。用户无需复杂配置即可在本地机器上运行量化后的开源模型，是个人开发者和隐私敏感场景的常用选择。

## 近期动态

- **Ollama v0.32.6-rc0**（2026-08-05）：优化苹果 GPU 推测解码速度，但暂时移除了图像生成功能。
- **Ollama v0.32.7**（2026-08-10）：新增 Muse Glimmer 模型支持，仅限 Apple Silicon MLX 引擎。

## 注意事项

- Apple Silicon 平台支持较好（MLX 引擎），NVIDIA、AMD 等平台的支持可能滞后。
- 运行大参数模型时需注意内存限制，社区建议适当调大 context size。
- 量化版本在精度和速度之间需要权衡，具体表现因模型和任务而异。

## 相关页面

- [[LLM Wiki]]
