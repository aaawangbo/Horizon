---
type: tool
status: growing
created: 2026-08-02
updated: 2026-08-02
confidence: high
sources: []
tags:
  - horizon
  - information-radar
  - automation
---

# Horizon

## 定位

Horizon 是本系统的信息雷达。它从官方博客、研究 RSS、GitHub Releases、Hacker News、Reddit 和开源趋势中抓取 AI 资讯，再调用 DeepSeek 进行筛选、评分和中文摘要。

## 当前配置

- 每天北京时间 08:30 自动运行。
- 默认输出中文。
- 最多保留 20 条高价值信息。
- 重点覆盖官方发布、研究论文、行业分析和开源项目。
- 公开页面：[AI 信息站](https://aaawangbo.github.io/Horizon/)
- 中文 Feed：[feed-zh.xml](https://aaawangbo.github.io/Horizon/feed-zh.xml)

## 在知识库中的职责

Horizon 负责扩大信息视野和降低初筛成本，但它生成的日报仍属于待核验资料。自动迭代流程读取 Feed 后，才把内容保存到原始资料层并更新知识页。

## 边界

- Horizon 的摘要不是最终事实来源。
- 发布前应打开日报中的原始链接核验。
- 自动评分反映预设偏好，不代表信息的绝对重要性。

## 相关页面

- [[AI 博主内容系统]]
- [[LLM Wiki]]
