# AI 博主版 Horizon

本 fork 已配置为中文 AI 博主选题雷达。

## 默认行为

- 每天北京时间 08:30 运行；
- 汇总最近 30 小时的信息；
- 最多保留 20 条，评分阈值为 7/10；
- 自动合并重复话题；
- 输出简体中文；
- 为每条重要信息补充“为什么重要”和“可创作角度”。

## 信息源

- OpenAI、Google DeepMind、Hugging Face 官方 RSS；
- Simon Willison、arXiv `cs.AI` 与 `cs.CL`；
- 量子位、新智元；
- Hacker News、Reddit `MachineLearning` 与 `LocalLLaMA`；
- OpenAI SDK、Transformers、Ollama、vLLM、LangChain、Open WebUI 的 GitHub Release；
- OSS Insight AI 开源趋势。

Twitter/X、Telegram、邮件和 Webhook 默认关闭，避免缺少凭据或产生额外费用。

## 必需 Secret

在仓库的 `Settings → Secrets and variables → Actions` 中创建：

```text
DEEPSEEK_API_KEY
```

密钥只保存在 GitHub Actions Secret 中，不应写进仓库文件。

## 手动运行

打开仓库的 `Actions` 页面，选择 `Daily AI Blogger Horizon`，点击 `Run workflow`。

工作流成功后会把生成的站点发布到 `gh-pages` 分支。首次运行后，在仓库的 `Settings → Pages` 中选择从 `gh-pages` 分支发布。

## 本地运行

```powershell
Copy-Item data/config.ai-blogger.json data/config.json
uv sync
uv run horizon --hours 30
```

本地密钥应放在仓库根目录的 `.env`：

```dotenv
DEEPSEEK_API_KEY=你的密钥
```

`.env` 和 `data/config.json` 已被上游 `.gitignore` 忽略。
