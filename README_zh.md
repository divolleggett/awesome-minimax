# Awesome MiniMax M2 系列

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![MiniMax](https://img.shields.io/badge/MiniMax-M2_Series-blue?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZD0iTTEyIDJMMiAxOWgyMEwxMiAyeiIgZmlsbD0iI2ZmZiIvPjwvc3ZnPg==)](https://www.minimaxi.com)
[![Atlas Cloud](https://img.shields.io/badge/Atlas_Cloud-立即体验-green?logo=cloud)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/ristponex/awesome-minimax/pulls)

[English](README.md) | **[中文](README_zh.md)** | [日本語](README_ja.md) | [한국어](README_ko.md)

---

> **MiniMax M2.7 即将发布！本页面追踪 M2 系列的所有动态。**

---

精心整理的 **MiniMax M2 系列**大语言模型相关资源、基准测试、工具和社区项目列表，涵盖 M2、M2.1、M2.5 以及即将推出的 M2.7。

## 目录

- [什么是 MiniMax M2？](#什么是-minimax-m2)
- [M2 系列演进](#m2-系列演进)
- [核心能力](#核心能力)
- [性能基准](#性能基准)
- [M2.7 展望](#m27-展望)
- [在 Atlas Cloud 上体验 MiniMax](#在-atlas-cloud-上体验-minimax)
- [API 快速入门](#api-快速入门)
- [定价](#定价)
- [M3 路线图](#m3-路线图)
- [社区资源](#社区资源)
- [常见问题](#常见问题)
- [贡献指南](#贡献指南)

## 什么是 MiniMax M2？

MiniMax M2 是一系列基于 **混合专家（MoE）架构** 的开源大语言模型。M2 系列拥有 **2300 亿总参数**，但每次推理仅激活 **100 亿参数**，以极低的计算成本实现前沿水平的性能。

核心架构特点：

- **MoE 设计** — 2300 亿总参数 / 100 亿激活参数，实现高质量输出与低延迟
- **开源** — 基于 Apache 2.0 许可证发布，完全支持商业使用
- **长上下文** — 支持扩展上下文窗口，适用于复杂推理任务
- **多语言** — 在中文、英文、日文、韩文等多种语言上表现优异
- **代码原生** — 针对 10+ 种编程语言的编程任务进行了专项训练

M2 系列经历了多次快速迭代，每次都在速度、编码能力和智能体能力方面带来显著提升。

## M2 系列演进

| 版本 | 发布时间 | 亮点 | 许可证 |
|------|---------|------|--------|
| **M2** | 2025年10月 | 首次开源发布。MoE 架构，2300亿/100亿参数。在推理、编码和多语言任务上建立强大基准。 | Apache 2.0 |
| **M2.1** | 2025年12月 | 增强多语言支持。改进编码能力。更好的指令遵循和减少幻觉。 | Apache 2.0 |
| **M2.5** | 2026年2月 | SWE-Bench 80.2%，BrowseComp 76.3%。推理速度比 M2 快 37%。达到最先进的智能体和工具调用性能。 | Apache 2.0 |
| **M2.7** | 即将推出 | 基于 M2 发展轨迹的预期改进。预计将进一步提升速度和能力。 | 待定 |

## 核心能力

### 卓越的编码能力

MiniMax M2.5 在 **10+ 种编程语言**上表现出色，包括 Python、JavaScript、TypeScript、Java、C++、Go、Rust、PHP、Ruby 和 Swift。在真实世界的软件工程基准测试中取得顶级成绩。

- **SWE-Bench Verified**：80.2% — 自主解决真实 GitHub issue
- **Multi-SWE-Bench**：51.3% — 处理多仓库代码库
- **HumanEval+**：代码生成任务高通过率
- **代码审查与重构** — 理解复杂代码库并提出改进建议

### 智能体与工具调用

M2.5 专为智能体工作流设计：

- **原生函数调用** — 结构化工具使用，支持 JSON schema
- **多步骤规划** — 将复杂任务分解为可执行步骤
- **网页浏览** — BrowseComp 76.3% 展示了强大的网页导航能力
- **API 编排** — 链式调用多个 API 以完成任务

### 推理与规划

- **思维链推理** — 在数学和逻辑基准测试上表现优异
- **长上下文理解** — 处理并推理长文档
- **任务分解** — 将复杂问题拆分为可管理的子任务

## 性能基准

**MiniMax M2.5**（当前最新稳定版本）的性能数据：

| 基准测试 | 分数 | 类别 |
|---------|------|------|
| SWE-Bench Verified | **80.2%** | 软件工程 |
| Multi-SWE-Bench | **51.3%** | 多仓库工程 |
| BrowseComp | **76.3%** | 网页浏览与导航 |
| 推理速度 | **100 tokens/sec**（原生） | 吞吐量 |

### 各版本速度提升

| 版本 | 相对速度 | 备注 |
|------|---------|------|
| M2 | 1.0x（基准） | 首次发布 |
| M2.1 | ~1.15x | 小幅优化 |
| M2.5 | **1.37x** | 比 M2 快 37% |
| M2.7 | 待定 | 预计进一步提升 |

## M2.7 展望

虽然 MiniMax 尚未正式公布 M2.7 的规格，但我们可以基于 M2 系列的发展轨迹做出合理预测：

### 发展规律

M2 系列的每个版本都带来了可量化的改进：

- **M2 到 M2.1**：更好的多语言支持、改进的编码能力、减少幻觉
- **M2.1 到 M2.5**：基准测试大幅提升（SWE-Bench 80.2%）、速度提升 37%、智能体能力
- **M2.5 到 M2.7**：预计将延续这一上升趋势

### 我们的预期

基于已确立的模式和 MiniMax CEO 的公开声明：

1. **进一步提升速度** — 每次迭代都更快。M2.7 可能原生推理速度超过 130+ tokens/sec。
2. **更强的编码基准** — SWE-Bench 分数稳步攀升。M2.7 可能目标在 SWE-Bench Verified 上达到 83%+。
3. **增强的智能体能力** — 工具调用和多步骤规划是 MiniMax 的重点方向。
4. **更好的推理能力** — 改进的思维链和数学推理。
5. **M3 的过渡版本** — MiniMax CEO 已确认 M3 将于 2026 年上半年发布。M2.7 可能是过渡版本，融入了为 M3 规划的关键架构改进。

> **M2.7 发布后将立即在 [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) 上可用。** 一旦有详细信息公布，我们将更新此页面。

## 在 Atlas Cloud 上体验 MiniMax

[Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) 通过 OpenAI 兼容的 API 提供快速、经济的 MiniMax M2 系列模型访问。

**为什么选择 Atlas Cloud？**

- **最低价格** — M2.5 仅需 $0.27 / $0.95 每百万 tokens（输入/输出）
- **OpenAI 兼容 API** — 从 GPT 或 Claude 切换只需一行代码
- **高吞吐量** — 优化的基础设施，提供快速推理
- **付费计划无速率限制** — 无限制扩展
- **所有 M2 版本可用** — 立即访问 M2、M2.1 和 M2.5

[![在 Atlas Cloud 上体验](https://img.shields.io/badge/体验_MiniMax-Atlas_Cloud-green?style=for-the-badge&logo=cloud)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)

## API 快速入门

Atlas Cloud 上的 MiniMax 使用 **OpenAI 兼容 API**，集成非常简便。

### Python

```python
from openai import OpenAI

client = OpenAI(
    api_key="your-atlas-cloud-api-key",
    base_url="https://api.atlascloud.ai/v1"
)

response = client.chat.completions.create(
    model="minimax-m2.5",
    messages=[
        {"role": "system", "content": "你是一个有帮助的编程助手。"},
        {"role": "user", "content": "用 Python 写一个使用埃拉托斯特尼筛法找出所有小于 n 的质数的函数。"}
    ],
    temperature=0.7,
    max_tokens=2048
)

print(response.choices[0].message.content)
```

### cURL

```bash
curl https://api.atlascloud.ai/v1/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer your-atlas-cloud-api-key" \
  -d '{
    "model": "minimax-m2.5",
    "messages": [
      {"role": "system", "content": "你是一个有帮助的编程助手。"},
      {"role": "user", "content": "解释 JavaScript 中 async/await 和 Promise 的区别。"}
    ],
    "temperature": 0.7,
    "max_tokens": 2048
  }'
```

### Node.js

```javascript
import OpenAI from "openai";

const client = new OpenAI({
  apiKey: "your-atlas-cloud-api-key",
  baseURL: "https://api.atlascloud.ai/v1",
});

const response = await client.chat.completions.create({
  model: "minimax-m2.5",
  messages: [
    { role: "system", content: "你是一个有帮助的编程助手。" },
    { role: "user", content: "用 Express.js 创建一个带输入验证的 REST API 端点。" },
  ],
  temperature: 0.7,
  max_tokens: 2048,
});

console.log(response.choices[0].message.content);
```

## 定价

MiniMax M2.5 最大的优势之一是其**出色的性价比**。得益于 MoE 架构（2300 亿总参数中仅激活 100 亿），推理成本远低于同类模型。

| 模型 | 输入（每百万 tokens） | 输出（每百万 tokens） | 架构 |
|------|---------------------|---------------------|------|
| **MiniMax M2.5** | **$0.27** | **$0.95** | MoE 2300亿/100亿 |
| GPT-4o | $2.50 | $10.00 | 稠密 |
| Claude 3.5 Sonnet | $3.00 | $15.00 | 稠密 |
| DeepSeek V3 | $0.27 | $1.10 | MoE |

> MiniMax M2.5 以前沿级别的编码性能，价格比 GPT-4o 和 Claude 3.5 Sonnet **低 90%**。

**访问 [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) 获取最优惠的 MiniMax 定价。**

## M3 路线图

MiniMax CEO 已确认 **M3 计划于 2026 年上半年发布**。以下是目前已知信息：

- **多模态融合** — M3 预计将原生支持文本、图像、音频和视频模态
- **更高效率** — 持续改进 MoE 架构以获得更好的性价比
- **更强推理** — 目标在复杂推理基准测试上达到下一个水平
- **M2.7 作为过渡** — M2.7 可能融入了早期 M3 的创新，作为技术过渡

我们会随着更多细节的发布更新此部分。给这个仓库加 Star 以保持关注！

## 社区资源

### 官方资源

- [MiniMax 官方网站](https://www.minimaxi.com) — 官方公司页面
- [MiniMax 海螺 AI](https://hailuoai.com) — MiniMax 消费级 AI 产品
- [MiniMax API 文档](https://www.minimaxi.com/document/introduction) — 官方 API 文档
- [MiniMax on Hugging Face](https://huggingface.co/MiniMaxAI) — 模型权重和演示

### 技术论文与文章

- [MiniMax-01 技术报告](https://arxiv.org/abs/2501.08313) — 原始架构论文
- [M2 系列技术报告](https://www.minimaxi.com/news/minimax-m2-series) — 官方 M2 系列详情

### 社区项目

- [MiniMax Cookbook](https://github.com/MiniMax-AI) — 官方示例和教程
- [Awesome LLM](https://github.com/Hannibal046/Awesome-LLM) — 综合 LLM 资源列表

### 工具与集成

- [LiteLLM](https://github.com/BerriAI/litellm) — 支持 100+ LLM 的统一 API（包括 MiniMax）
- [OpenRouter](https://openrouter.ai/) — 多模型 API 网关
- [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) — 经济实惠的 MiniMax API 访问

## 常见问题

### MiniMax M2 与其他 LLM 有什么不同？

MiniMax M2 采用**混合专家（MoE）架构**，拥有 2300 亿总参数，但推理时仅激活 100 亿。这意味着你可以以运行 100 亿模型的成本获得 2300 亿模型的质量。结合 Apache 2.0 许可证和强大的编码基准，它是目前最具性价比的前沿模型之一。

### MiniMax M2 是开源的吗？

是的。MiniMax M2、M2.1 和 M2.5 都在 **Apache 2.0 许可证**下发布，允许商业使用、修改和再分发。

### M2.5 的编码能力与 GPT-4o 相比如何？

M2.5 在 **SWE-Bench Verified 上达到 80.2%**，在真实世界的软件工程任务上与 GPT-4o 相当或超越。以每百万 tokens $0.27/$0.95 的价格，同等编码质量下**便宜约 10 倍**。

### M2.7 什么时候发布？

目前没有官方发布日期。根据之前的发布节奏（2025年10月、2025年12月、2026年2月），M2.7 可能在 **2026 年第二季度**到来。一旦有官方信息，我们将更新此页面。

### 可以用现有的 OpenAI 代码使用 MiniMax M2 吗？

可以！通过 [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)，MiniMax M2 提供 **OpenAI 兼容 API**。你只需修改 `base_url` 和 `api_key`，现有代码即可直接使用。

### M2.5 支持哪些编程语言？

M2.5 支持 **10+ 种编程语言**，包括 Python、JavaScript、TypeScript、Java、C++、Go、Rust、PHP、Ruby 和 Swift，在 Python 和 JavaScript 上表现尤为突出。

### M2.5 适合构建 AI 智能体吗？

非常适合。M2.5 在**函数调用**、**多步骤规划**和**网页浏览**（BrowseComp 76.3%）方面表现出色。考虑到其低成本，它是智能体工作流中最有能力的模型之一。

### MiniMax M3 是什么？

M3 是 MiniMax 的下一代模型，CEO 已确认将于 **2026 年上半年**发布。预计将具备多模态能力和进一步改进的 MoE 架构。M2.7 可能是融入早期 M3 创新的过渡版本。

## 贡献指南

欢迎贡献！请遵循以下准则：

1. **Fork** 此仓库
2. **创建**一个新分支用于你的贡献
3. **提交** Pull Request，附上清晰的描述
4. 确保你的贡献遵循 [Awesome list 准则](https://github.com/sindresorhus/awesome/blob/main/contributing.md)

---

## 保持更新

- **Star** 此仓库以获取 M2.7 和 M3 的更新通知
- **Watch** 以接收发布通知
- **关注** [MiniMax](https://www.minimaxi.com) 获取官方公告

---

**准备好体验 MiniMax M2.5 了吗？** 访问 [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) — 以最实惠的价格通过 OpenAI 兼容 API 访问 MiniMax 模型。

[![在 Atlas Cloud 上开始](https://img.shields.io/badge/开始使用-Atlas_Cloud-green?style=for-the-badge&logo=cloud)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)
