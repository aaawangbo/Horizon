---
type: concept
status: seed
created: 2026-08-02
updated: 2026-08-02
confidence: high
sources:
  - "[[2026-04-04 Karpathy - LLM Wiki]]"
tags:
  - rag
  - retrieval
  - llm
---

# RAG

## 定义

RAG（Retrieval-Augmented Generation）通常在回答问题时，从外部资料中检索相关片段，再让模型基于这些片段生成答案。

## 优点

- 原始资料很多时，可以按需取回相关内容。
- 不需要把全部材料放进模型上下文。
- 适合寻找具体事实和处理更新频繁的文档集合。

## 局限

- 多文档综合往往在每次查询时重新发生，之前的理解不一定被保留。
- 检索质量受分块、索引、关键词和相似度影响。
- 隐含关系、矛盾和长期演变不一定能靠一次检索发现。

## 与 LLM Wiki 的关系

[[LLM Wiki]] 不应该被理解为完全替代 RAG。Wiki 负责持久综合，RAG 或本地搜索负责在规模扩大后定位来源和页面。两者可以组合：先检索，再把经过验证的综合结果写回 Wiki。

## 相关页面

- [[LLM Wiki]]
- [[知识复利]]
