---
type: tool
status: seed
created: 2026-08-11
updated: 2026-08-11
confidence: medium
sources:
  - "[[2026-08-11 Horizon Summary- 2026-08-11 (ZH) (b6971f89)]]"
tags:
  - vllm
  - inference
  - model-serving
  - open-source
---

# vLLM

## 概述

vLLM 是一个高吞吐量、内存高效的 LLM 推理与服务引擎，支持 200+ 模型架构，是 AI 基础设施领域的重要开源项目。

## v0.27.0（2026-08-10 发布）

- **规模**：561 个提交，242 位贡献者（64 位新贡献者）。
- **新增模型支持**：Kimi K3（完整推理支持，含 Python/Rust 前端、AttnRes 内核、DeepGEMM、compressed-tensors 量化检查点、可选共享专家分片）；Qwen3.5 文本模型、K-EXAONE-2.0-750B-A37B、VaultGemma、jina-embeddings-v5-text-nano。
- **DeepSeek-V4 优化**：序列并行、跳过空 c128 启动（约 2 倍内核提升）、跳过解码期 topk/router（3.4% E2E TTFT）、工作区复用（3.9% E2E TTFT）、移除冗余全内核（1.88 倍内核提升）等。
- **PyTorch 升级**：2.13.0（torchvision 0.28.0、Triton 3.7.1），官方标注为破坏性环境变化。
- **FlashAttention 4**：SM100 上新增 FP8 KV cache 与 headdim-256 支持，加入 JIT 预热机制。
- **移除/弃用**：移除 Plamo2、Ouro 模型，弃用 max_num_partial_prefills 等参数。

## 部署注意事项

- 官方镜像目前只有 CUDA 13（cu130）构建，要求 r580+ 驱动，CUDA 12.9 主机无法直接使用。
- 升级前需检查 PyTorch 2.13/Triton 3.7.1 的兼容性。

## 相关页面
- [[DeepSeek]]
- 同类本地推理工具：[[Ollama]]
- [[2026-08-11 AI 趋势综合]]
- [[AI 博主内容系统]]
