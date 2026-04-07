# Awesome MiniMax M2 Series

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![MiniMax](https://img.shields.io/badge/MiniMax-M2_Series-blue?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZD0iTTEyIDJMMiAxOWgyMEwxMiAyeiIgZmlsbD0iI2ZmZiIvPjwvc3ZnPg==)](https://www.minimaxi.com)
[![Atlas Cloud](https://img.shields.io/badge/Atlas_Cloud-Try_Now-green?logo=cloud)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/divolleggett/awesome-minimax/pulls)

**[English](README.md)** | [中文](README_zh.md) | [日本語](README_ja.md) | [한국어](README_ko.md)

---

> 🔥 **MiniMax M2.7 is now available!** Self-evolving AI — 90% of Opus 4.6 quality at 7% cost. [Try on Atlas Cloud →](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)

---

A curated list of resources, benchmarks, tools, and community projects related to the **MiniMax M2 series** of large language models — including M2, M2.1, M2.5, and the latest **M2.7** (released March 18, 2026).

## Table of Contents

- [What is MiniMax M2?](#what-is-minimax-m2)
- [M2 Series Evolution](#m2-series-evolution)
- [Key Capabilities](#key-capabilities)
- [Performance Benchmarks](#performance-benchmarks)
- [M2.7 — What's New](#-m27--whats-new-released-march-18-2026)
- [Try MiniMax on Atlas Cloud](#try-minimax-on-atlas-cloud)
- [API Quick Start](#api-quick-start)
- [Pricing](#pricing)
- [M3 Roadmap](#m3-roadmap)
- [Community Resources](#community-resources)
- [FAQ](#faq)
- [Contributing](#contributing)

## What is MiniMax M2?

MiniMax M2 is a family of open-source large language models built on a **Mixture-of-Experts (MoE)** architecture. The M2 series features **230 billion total parameters** with only **10 billion active parameters** per inference pass, delivering frontier-level performance at a fraction of the compute cost.

Key architectural highlights:

- **MoE Design** — 230B total / 10B active parameters, enabling high-quality output with low latency
- **Open Source** — Released under the Apache 2.0 license, fully open for commercial use
- **Long Context** — Supports extended context windows for complex reasoning tasks
- **Multilingual** — Strong performance across English, Chinese, Japanese, Korean, and many other languages
- **Code-Native** — Trained with a focus on programming tasks across 10+ languages

The M2 series has rapidly evolved through multiple iterations, each bringing significant improvements in speed, coding ability, and agent capabilities.

## M2 Series Evolution

| Version | Release | Highlights | License |
|---------|---------|------------|---------|
| **M2** | Oct 2025 | First open-source release. MoE architecture with 230B/10B params. Strong baseline across reasoning, coding, and multilingual tasks. | Apache 2.0 |
| **M2.1** | Dec 2025 | Enhanced multilingual support. Improved coding capabilities. Better instruction following and reduced hallucinations. | Apache 2.0 |
| **M2.5** | Feb 2026 | SWE-Bench 80.2%, BrowseComp 76.3%. 37% faster inference than M2. State-of-the-art agent and tool-calling performance. | Apache 2.0 |
| **M2.7** | Mar 2026 | 🔥 Self-evolution capability (100+ autonomous optimization rounds). SWE-Pro 56.22% (matches GPT-5.3-Codex). Hallucination reduced from -40 to +1 on AA-Omniscience. 97% skill compliance. 204K context. | Proprietary (API only) |

## Key Capabilities

### Coding Excellence

MiniMax M2.5 excels across **10+ programming languages** including Python, JavaScript, TypeScript, Java, C++, Go, Rust, PHP, Ruby, and Swift. It achieves top-tier results on real-world software engineering benchmarks.

- **SWE-Bench Verified**: 80.2% — solves real GitHub issues autonomously
- **Multi-SWE-Bench**: 51.3% — handles multi-repository codebases
- **HumanEval+**: High pass rates on code generation tasks
- **Code review and refactoring** — understands complex codebases and suggests improvements

### Agent & Tool Calling

M2.5 is designed for agentic workflows:

- **Native function calling** — structured tool use with JSON schema support
- **Multi-step planning** — breaks down complex tasks into executable steps
- **Web browsing** — BrowseComp 76.3% demonstrates strong web navigation abilities
- **API orchestration** — chains multiple API calls to complete tasks

### Reasoning & Planning

- **Chain-of-thought reasoning** — strong performance on mathematical and logical benchmarks
- **Long-context understanding** — processes and reasons over extended documents
- **Task decomposition** — breaks complex problems into manageable sub-tasks

## Performance Benchmarks

Performance data for **MiniMax M2.5** (the current latest stable release):

| Benchmark | Score | Category |
|-----------|-------|----------|
| SWE-Bench Verified | **80.2%** | Software Engineering |
| Multi-SWE-Bench | **51.3%** | Multi-Repo Engineering |
| BrowseComp | **76.3%** | Web Browsing & Navigation |
| Inference Speed | **100 tokens/sec** (native) | Throughput |

### Speed Improvements Across Versions

| Version | Relative Speed | Notes |
|---------|---------------|-------|
| M2 | 1.0x (baseline) | Initial release |
| M2.1 | ~1.15x | Minor optimizations |
| M2.5 | **1.37x** | 37% faster than M2 |
| M2.7 | TBD | Further improvements expected |

## 🔥 M2.7 — What's New (Released March 18, 2026)

M2.7 is the first model in the M2 series to deeply participate in its own evolution.

### Self-Evolution — The Headline Feature

M2.7 ran **100+ scaffold optimization rounds autonomously** using the OpenClaw (Agent Harness) framework, achieving a **30% performance boost** without human intervention. It can automate **30-50% of reinforcement learning research workflows**, including experiment configuration, data pipeline management, and training code modification.

### Key Improvements over M2.5

| Metric | M2.5 | M2.7 | Change |
|--------|------|------|--------|
| **SWE-Pro** | — | **56.22%** | Matches GPT-5.3-Codex |
| **SWE-bench Verified** | 80.2% | **78%** | Comparable |
| **AA-Omniscience (Hallucination)** | -40 | **+1** | Massive improvement |
| **MM Claw (Skill Compliance)** | — | **97%** | 40+ complex skills |
| **VIBE-Pro** | — | **55.6%** | Near Opus 4.6 |
| **Terminal Bench 2** | — | **57.0%** | System-level understanding |
| **Context Window** | 128K | **204K** | 60% larger |
| **Max Output** | — | **131K** | — |

### Cost vs Quality

M2.7 delivers **~90% of Claude Opus 4.6 quality at only 7% of the cost**, running 3x faster.

| Model | Input/M tokens | Output/M tokens | SWE-Pro |
|-------|---------------|----------------|---------|
| **MiniMax M2.7** | **$0.30** | **$1.20** | **56.22%** |
| Claude Opus 4.6 | $15.00 | $75.00 | ~56% |
| GPT-5.3-Codex | — | — | 56.22% |

### Supported Integrations (11+ tools)

M2.7 works with: **Claude Code**, **Cursor**, **OpenClaw**, **Cline**, **Roo Code**, **Kilo Code**, **Codex CLI**, **TRAE**, **Zed**, **Droid**, **Grok CLI**, **OpenCode**

> 🚀 **M2.7 is available now on [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)** — model ID: `minimaxai/minimax-m2.7`

## Try MiniMax on Atlas Cloud

[Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) provides fast, affordable access to MiniMax M2 series models via an OpenAI-compatible API.

**Why Atlas Cloud?**

- **Lowest pricing** — M2.5 at $0.27 / $0.95 per million tokens (input/output)
- **OpenAI-compatible API** — switch from GPT or Claude with a one-line code change
- **High throughput** — optimized infrastructure for fast inference
- **No rate limits on paid plans** — scale without restrictions
- **All M2 versions available** — access M2, M2.1, and M2.5 today

[![Try on Atlas Cloud](https://img.shields.io/badge/Try_MiniMax-Atlas_Cloud-green?style=for-the-badge&logo=cloud)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)

## API Quick Start

MiniMax on Atlas Cloud uses an **OpenAI-compatible API**, making integration easy.

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
        {"role": "system", "content": "You are a helpful coding assistant."},
        {"role": "user", "content": "Write a Python function to find all prime numbers up to n using the Sieve of Eratosthenes."}
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
      {"role": "system", "content": "You are a helpful coding assistant."},
      {"role": "user", "content": "Explain the difference between async/await and Promises in JavaScript."}
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
    { role: "system", content: "You are a helpful coding assistant." },
    { role: "user", content: "Create a REST API endpoint in Express.js with input validation." },
  ],
  temperature: 0.7,
  max_tokens: 2048,
});

console.log(response.choices[0].message.content);
```

## Pricing

One of the biggest advantages of MiniMax M2.5 is its **exceptional cost-effectiveness**. Thanks to the MoE architecture (only 10B active params out of 230B total), inference costs are dramatically lower than comparable models.

| Model | Input (per 1M tokens) | Output (per 1M tokens) | Architecture |
|-------|----------------------|------------------------|--------------|
| **MiniMax M2.5** | **$0.27** | **$0.95** | MoE 230B/10B |
| GPT-4o | $2.50 | $10.00 | Dense |
| Claude 3.5 Sonnet | $3.00 | $15.00 | Dense |
| DeepSeek V3 | $0.27 | $1.10 | MoE |

> MiniMax M2.5 delivers frontier-level coding performance at **up to 90% less** than GPT-4o and Claude 3.5 Sonnet.

**Get started with [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) for the best MiniMax pricing.**

## M3 Roadmap

MiniMax CEO has confirmed that **M3 is planned for H1 2026**. Here's what we know:

- **Multimodal Fusion** — M3 is expected to natively support text, image, audio, and video modalities
- **Higher Efficiency** — Continued improvements to the MoE architecture for better cost-performance ratio
- **Stronger Reasoning** — Targeting next-level performance on complex reasoning benchmarks
- **M2.7 as a Bridge** — M2.7 likely incorporates early M3 innovations, serving as a stepping stone

We'll update this section as more details emerge. Star this repo to stay informed!

## Community Resources

### Official Resources

- [MiniMax Official Website](https://www.minimaxi.com) — Official company page
- [MiniMax Hailuo AI](https://hailuoai.com) — MiniMax consumer AI product
- [MiniMax API Docs](https://www.minimaxi.com/document/introduction) — Official API documentation
- [MiniMax on Hugging Face](https://huggingface.co/MiniMaxAI) — Model weights and demos

### Technical Papers & Articles

- [MiniMax-01 Technical Report](https://arxiv.org/abs/2501.08313) — Original architecture paper
- [M2 Series Technical Report](https://www.minimaxi.com/news/minimax-m2-series) — Official M2 series details

### Community Projects

- [MiniMax Cookbook](https://github.com/MiniMax-AI) — Official examples and tutorials
- [Awesome LLM](https://github.com/Hannibal046/Awesome-LLM) — Comprehensive LLM resource list

### Video Tutorials

- [MiniMax M2.5 Deep Dive](https://www.youtube.com/results?search_query=minimax+m2.5) — Community video reviews
- [MoE Architecture Explained](https://www.youtube.com/results?search_query=mixture+of+experts+explained) — Understanding the technology behind M2

### Tools & Integrations

- [LiteLLM](https://github.com/BerriAI/litellm) — Unified API for 100+ LLMs including MiniMax
- [OpenRouter](https://openrouter.ai/) — Multi-model API gateway
- [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) — Affordable MiniMax API access

## FAQ

### What makes MiniMax M2 different from other LLMs?

MiniMax M2 uses a **Mixture-of-Experts (MoE) architecture** with 230B total parameters but only 10B active during inference. This means you get the quality of a 230B model at the cost of running a 10B model. Combined with its Apache 2.0 license and strong coding benchmarks, it's one of the most cost-effective frontier models available.

### Is MiniMax M2 open source?

Yes. MiniMax M2, M2.1, and M2.5 are all released under the **Apache 2.0 license**, which permits commercial use, modification, and redistribution.

### How does M2.5 compare to GPT-4o for coding?

M2.5 achieves **80.2% on SWE-Bench Verified**, which is competitive with or exceeds GPT-4o on real-world software engineering tasks. At $0.27/$0.95 per million tokens, it's roughly **10x cheaper** for comparable coding quality.

### Is M2.7 available now?

Yes! M2.7 was released on **March 18, 2026**. It's available via [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) (model ID: `minimaxai/minimax-m2.7`), MiniMax Platform, and OpenRouter. Its headline feature is **self-evolution** — the model autonomously ran 100+ optimization rounds, achieving 30% performance gains without human intervention.

### Can I use MiniMax M2 with existing OpenAI code?

Yes! Through [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax), MiniMax M2 is available via an **OpenAI-compatible API**. You only need to change the `base_url` and `api_key` — your existing code works as-is.

### What languages does M2.5 support for coding?

M2.5 supports **10+ programming languages** including Python, JavaScript, TypeScript, Java, C++, Go, Rust, PHP, Ruby, and Swift, with particularly strong performance in Python and JavaScript.

### Is M2.5 good for building AI agents?

Absolutely. M2.5 excels at **function calling**, **multi-step planning**, and **web browsing** (76.3% on BrowseComp). It's one of the most capable models for agentic workflows, especially considering its low cost.

### What is MiniMax M3?

M3 is the next-generation model from MiniMax, confirmed by the CEO for **H1 2026**. It's expected to feature multimodal capabilities and further improvements to the MoE architecture. M2.7 is likely a bridge release incorporating early M3 innovations.

## Contributing

Contributions are welcome! Please read the following guidelines:

1. **Fork** this repository
2. **Create** a new branch for your contribution
3. **Submit** a pull request with a clear description
4. Ensure your contribution follows the [Awesome list guidelines](https://github.com/sindresorhus/awesome/blob/main/contributing.md)

Types of contributions we're looking for:

- New community projects, tools, or integrations
- Updated benchmark data
- Tutorials and guides
- Translations
- Bug fixes and improvements

---

## Stay Updated

- **Star** this repo to get notified about M2.7 and M3 updates
- **Watch** for release notifications
- **Follow** [MiniMax](https://www.minimaxi.com) for official announcements

---

**Ready to try MiniMax M2.5?** Get started on [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) — the most affordable way to access MiniMax models with an OpenAI-compatible API.

[![Try on Atlas Cloud](https://img.shields.io/badge/Get_Started-Atlas_Cloud-green?style=for-the-badge&logo=cloud)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)
