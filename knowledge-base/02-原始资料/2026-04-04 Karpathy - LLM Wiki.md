---
type: source
source_id: gist-karpathy-442a6bf555914893e9891c11519de94f
source_type: article
title: LLM Wiki
author: Andrej Karpathy
url: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
published: 2026-04-04
captured: 2026-08-02
processed: true
language: en
tags:
  - llm-wiki
  - knowledge-management
  - obsidian
  - agents
---

# LLM Wiki — Andrej Karpathy

## 来源说明

这是一份面向 LLM Agent 的设计说明，而不是某个具体产品教程。作者提出：让智能体持续维护一套结构化 Markdown Wiki，使知识在多次阅读和提问中累积，而不是每次查询都从原始文档重新检索和拼接。

原文：[LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)

## 关键主张

1. 传统 RAG 在查询时临时检索和综合，之前的综合过程通常不会沉淀。
2. LLM Wiki 是位于用户和原始资料之间的持久知识层，会随着新来源持续修订。
3. 系统应分为不可变原始资料、AI 维护的 Wiki、约束 AI 行为的 Schema 三层。
4. 核心操作是 Ingest、Query 和 Lint，而不是单纯“存笔记”。
5. `index.md` 用于按内容导航，`log.md` 用于按时间审计，两者职责不同。
6. 中小规模知识库可以先用索引和文本搜索，无需过早建设向量数据库。
7. 人负责选择来源、提出问题和做判断；LLM 负责摘要、交叉引用和维护工作。

## 对本知识库的直接影响

- 采用“来源—知识—规则”三层结构。
- 把 Obsidian 作为浏览与人工审核界面。
- 维护独立的 [[索引]] 与 [[日志]]。
- 引入自动 Lint 和规则提案机制。
- 将每次研究和问答中可复用的成果回写，而不是留在聊天记录里。

## 风险与保留意见

- Wiki 会放大错误：错误综合如果未被发现，之后可能被反复引用。
- 自动维护可能产生分类漂移、近义页面和失效交叉链接。
- 原文强调 Lint，但没有给出完整的事实核验和规则自修改安全方案。
- 因此本系统增加了证据字段、置信度、路径白名单和“规则只提案不自动生效”的限制。

## 关联知识

- [[LLM Wiki]]
- [[RAG]]
- [[知识复利]]
- [[AI 博主内容系统]]
- [[Andrej Karpathy]]
- [[Obsidian]]
