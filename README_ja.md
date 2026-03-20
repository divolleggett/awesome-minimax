# Awesome MiniMax M2 シリーズ

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![MiniMax](https://img.shields.io/badge/MiniMax-M2_Series-blue?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZD0iTTEyIDJMMiAxOWgyMEwxMiAyeiIgZmlsbD0iI2ZmZiIvPjwvc3ZnPg==)](https://www.minimaxi.com)
[![Atlas Cloud](https://img.shields.io/badge/Atlas_Cloud-今すぐ試す-green?logo=cloud)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/ristponex/awesome-minimax/pulls)

[English](README.md) | [中文](README_zh.md) | **[日本語](README_ja.md)** | [한국어](README_ko.md)

---

> **MiniMax M2.7 がまもなくリリース予定！このページでは M2 シリーズの全情報を追跡しています。**

---

**MiniMax M2 シリーズ**大規模言語モデルに関するリソース、ベンチマーク、ツール、コミュニティプロジェクトを厳選したリストです。M2、M2.1、M2.5、そして今後リリース予定の M2.7 を網羅しています。

## 目次

- [MiniMax M2 とは？](#minimax-m2-とは)
- [M2 シリーズの進化](#m2-シリーズの進化)
- [主要な機能](#主要な機能)
- [性能ベンチマーク](#性能ベンチマーク)
- [M2.7 への期待](#m27-への期待)
- [Atlas Cloud で MiniMax を試す](#atlas-cloud-で-minimax-を試す)
- [API クイックスタート](#api-クイックスタート)
- [料金](#料金)
- [M3 ロードマップ](#m3-ロードマップ)
- [コミュニティリソース](#コミュニティリソース)
- [よくある質問](#よくある質問)
- [コントリビューション](#コントリビューション)

## MiniMax M2 とは？

MiniMax M2 は、**Mixture-of-Experts（MoE）アーキテクチャ**に基づくオープンソースの大規模言語モデルファミリーです。M2 シリーズは**総パラメータ数 2,300 億**、推論時の**アクティブパラメータはわずか 100 億**で、計算コストの一部でフロンティアレベルの性能を実現します。

主要なアーキテクチャの特徴：

- **MoE 設計** — 2,300 億 / 100 億パラメータで、高品質な出力と低レイテンシーを実現
- **オープンソース** — Apache 2.0 ライセンスで公開、商用利用完全対応
- **ロングコンテキスト** — 複雑な推論タスクに対応する拡張コンテキストウィンドウ
- **多言語対応** — 英語、中国語、日本語、韓国語など多くの言語で高い性能
- **コードネイティブ** — 10 以上のプログラミング言語でのコーディングタスクに特化した学習

M2 シリーズは複数回の反復を経て急速に進化し、各バージョンで速度、コーディング能力、エージェント機能が大幅に向上しています。

## M2 シリーズの進化

| バージョン | リリース | ハイライト | ライセンス |
|-----------|---------|-----------|-----------|
| **M2** | 2025年10月 | 初のオープンソースリリース。MoE アーキテクチャ、2,300億/100億パラメータ。推論、コーディング、多言語タスクで強力なベースライン。 | Apache 2.0 |
| **M2.1** | 2025年12月 | 多言語サポートの強化。コーディング能力の改善。指示追従の向上とハルシネーションの削減。 | Apache 2.0 |
| **M2.5** | 2026年2月 | SWE-Bench 80.2%、BrowseComp 76.3%。M2 比 37% 高速化。最先端のエージェント・ツール呼び出し性能。 | Apache 2.0 |
| **M2.7** | 近日公開 | M2 の発展軌跡に基づく改善が期待。さらなる速度と能力の向上。 | 未定 |

## 主要な機能

### 卓越したコーディング能力

MiniMax M2.5 は Python、JavaScript、TypeScript、Java、C++、Go、Rust、PHP、Ruby、Swift を含む **10 以上のプログラミング言語**で優れた性能を発揮します。

- **SWE-Bench Verified**: 80.2% — 実際の GitHub issue を自律的に解決
- **Multi-SWE-Bench**: 51.3% — マルチリポジトリのコードベースを処理
- **HumanEval+**: コード生成タスクで高い合格率
- **コードレビュー・リファクタリング** — 複雑なコードベースを理解し改善を提案

### エージェント・ツール呼び出し

M2.5 はエージェントワークフロー向けに設計されています：

- **ネイティブ関数呼び出し** — JSON スキーマサポートによる構造化ツール使用
- **マルチステップ計画** — 複雑なタスクを実行可能なステップに分解
- **Web ブラウジング** — BrowseComp 76.3% で強力な Web ナビゲーション能力を実証
- **API オーケストレーション** — 複数の API 呼び出しを連鎖させてタスクを完了

### 推論・計画

- **思考の連鎖推論** — 数学・論理ベンチマークでの優れた性能
- **ロングコンテキスト理解** — 長文ドキュメントの処理と推論
- **タスク分解** — 複雑な問題を管理可能なサブタスクに分割

## 性能ベンチマーク

**MiniMax M2.5**（現在の最新安定版）の性能データ：

| ベンチマーク | スコア | カテゴリ |
|------------|-------|---------|
| SWE-Bench Verified | **80.2%** | ソフトウェアエンジニアリング |
| Multi-SWE-Bench | **51.3%** | マルチリポエンジニアリング |
| BrowseComp | **76.3%** | Web ブラウジング・ナビゲーション |
| 推論速度 | **100 tokens/sec**（ネイティブ） | スループット |

### バージョン別速度改善

| バージョン | 相対速度 | 備考 |
|-----------|---------|------|
| M2 | 1.0x（ベースライン） | 初期リリース |
| M2.1 | ~1.15x | 軽微な最適化 |
| M2.5 | **1.37x** | M2 比 37% 高速 |
| M2.7 | 未定 | さらなる改善が期待 |

## M2.7 への期待

MiniMax はまだ M2.7 の仕様を正式に発表していませんが、M2 シリーズの発展軌跡に基づいて合理的な予測が可能です：

### 進化のパターン

M2 シリーズの各バージョンは測定可能な改善をもたらしています：

- **M2 → M2.1**: 多言語サポートの向上、コーディング改善、ハルシネーション削減
- **M2.1 → M2.5**: ベンチマーク大幅向上（SWE-Bench 80.2%）、37% の高速化、エージェント機能
- **M2.5 → M2.7**: この上昇トレンドの継続が期待

### 予想される改善

確立されたパターンと MiniMax CEO の公開発言に基づく：

1. **さらなる速度向上** — 各バージョンで高速化。M2.7 はネイティブで 130+ tokens/sec を超える可能性。
2. **より強力なコーディングベンチマーク** — SWE-Bench スコアは着実に上昇。M2.7 は SWE-Bench Verified で 83%+ を目標にする可能性。
3. **強化されたエージェント機能** — ツール呼び出しとマルチステップ計画は MiniMax の重点分野。
4. **より優れた推論能力** — 改善された思考の連鎖と数学的推論。
5. **M3 への橋渡し** — MiniMax CEO は M3 を 2026 年上半期に確認。M2.7 は M3 向けの主要なアーキテクチャ改善を取り入れたブリッジリリースの可能性。

> **M2.7 はリリース時に [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) で利用可能になります。** 詳細が発表され次第、このページを更新します。

## Atlas Cloud で MiniMax を試す

[Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) は、OpenAI 互換 API を通じて MiniMax M2 シリーズモデルへの高速でお手頃なアクセスを提供します。

**Atlas Cloud を選ぶ理由：**

- **最安値の料金** — M2.5 は 100 万トークンあたり $0.27 / $0.95（入力/出力）
- **OpenAI 互換 API** — GPT や Claude からの切り替えはコード 1 行の変更のみ
- **高スループット** — 高速推論のための最適化されたインフラ
- **有料プランはレート制限なし** — 制約なくスケール
- **全 M2 バージョン利用可能** — M2、M2.1、M2.5 に今すぐアクセス

[![Atlas Cloud で試す](https://img.shields.io/badge/MiniMax_を試す-Atlas_Cloud-green?style=for-the-badge&logo=cloud)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)

## API クイックスタート

Atlas Cloud の MiniMax は **OpenAI 互換 API** を使用しており、統合が簡単です。

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
        {"role": "system", "content": "あなたは親切なコーディングアシスタントです。"},
        {"role": "user", "content": "エラトステネスの篩を使って n 以下の素数をすべて見つける Python 関数を書いてください。"}
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
      {"role": "system", "content": "あなたは親切なコーディングアシスタントです。"},
      {"role": "user", "content": "JavaScript における async/await と Promise の違いを説明してください。"}
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
    { role: "system", content: "あなたは親切なコーディングアシスタントです。" },
    { role: "user", content: "Express.js で入力バリデーション付きの REST API エンドポイントを作成してください。" },
  ],
  temperature: 0.7,
  max_tokens: 2048,
});

console.log(response.choices[0].message.content);
```

## 料金

MiniMax M2.5 の最大の利点の一つは、その**優れたコストパフォーマンス**です。MoE アーキテクチャ（2,300 億パラメータ中アクティブはわずか 100 億）により、推論コストは同等モデルと比較して大幅に低くなっています。

| モデル | 入力（100 万トークンあたり） | 出力（100 万トークンあたり） | アーキテクチャ |
|-------|--------------------------|--------------------------|--------------|
| **MiniMax M2.5** | **$0.27** | **$0.95** | MoE 2,300億/100億 |
| GPT-4o | $2.50 | $10.00 | Dense |
| Claude 3.5 Sonnet | $3.00 | $15.00 | Dense |
| DeepSeek V3 | $0.27 | $1.10 | MoE |

> MiniMax M2.5 はフロンティアレベルのコーディング性能を、GPT-4o や Claude 3.5 Sonnet の**最大 90% オフ**で提供します。

**[Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) で最高の MiniMax 料金をご利用ください。**

## M3 ロードマップ

MiniMax CEO は **M3 を 2026 年上半期に計画**していることを確認しています。現在判明していること：

- **マルチモーダル融合** — M3 はテキスト、画像、音声、動画モダリティのネイティブサポートが期待
- **さらなる効率化** — MoE アーキテクチャの継続的改善でコスト性能比を向上
- **より強力な推論** — 複雑な推論ベンチマークでの次世代レベルの性能を目標
- **M2.7 がブリッジに** — M2.7 は初期の M3 イノベーションを取り入れ、橋渡しとなる可能性

詳細が公開され次第このセクションを更新します。最新情報を得るために Star をお願いします！

## コミュニティリソース

### 公式リソース

- [MiniMax 公式サイト](https://www.minimaxi.com) — 公式企業ページ
- [MiniMax 海螺 AI](https://hailuoai.com) — MiniMax のコンシューマー AI 製品
- [MiniMax API ドキュメント](https://www.minimaxi.com/document/introduction) — 公式 API ドキュメント
- [MiniMax on Hugging Face](https://huggingface.co/MiniMaxAI) — モデルウェイトとデモ

### 技術論文・記事

- [MiniMax-01 技術レポート](https://arxiv.org/abs/2501.08313) — オリジナルアーキテクチャ論文
- [M2 シリーズ技術レポート](https://www.minimaxi.com/news/minimax-m2-series) — 公式 M2 シリーズ詳細

### コミュニティプロジェクト

- [MiniMax Cookbook](https://github.com/MiniMax-AI) — 公式サンプルとチュートリアル
- [Awesome LLM](https://github.com/Hannibal046/Awesome-LLM) — 包括的な LLM リソースリスト

### ツール・インテグレーション

- [LiteLLM](https://github.com/BerriAI/litellm) — MiniMax を含む 100+ LLM の統一 API
- [OpenRouter](https://openrouter.ai/) — マルチモデル API ゲートウェイ
- [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) — お手頃な MiniMax API アクセス

## よくある質問

### MiniMax M2 は他の LLM と何が違いますか？

MiniMax M2 は **Mixture-of-Experts（MoE）アーキテクチャ**を採用し、総パラメータ 2,300 億に対し推論時のアクティブパラメータはわずか 100 億です。100 億モデルのコストで 2,300 億モデルの品質を得られます。Apache 2.0 ライセンスと強力なコーディングベンチマークを合わせると、最もコストパフォーマンスの高いフロンティアモデルの一つです。

### MiniMax M2 はオープンソースですか？

はい。MiniMax M2、M2.1、M2.5 はすべて **Apache 2.0 ライセンス**でリリースされており、商用利用、改変、再配布が可能です。

### M2.5 のコーディング能力は GPT-4o と比べてどうですか？

M2.5 は **SWE-Bench Verified で 80.2%** を達成しており、実際のソフトウェアエンジニアリングタスクで GPT-4o と同等以上の性能です。100 万トークンあたり $0.27/$0.95 で、同等のコーディング品質が**約 10 分の 1 のコスト**で利用できます。

### M2.7 はいつリリースされますか？

公式のリリース日はまだ発表されていません。過去のリリース間隔（2025年10月、12月、2026年2月）から、M2.7 は **2026 年第2四半期**に登場する可能性があります。公式情報が入り次第、このページを更新します。

### 既存の OpenAI コードで MiniMax M2 を使えますか？

はい！[Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) を通じて、MiniMax M2 は **OpenAI 互換 API** で利用可能です。`base_url` と `api_key` を変更するだけで、既存のコードがそのまま動作します。

### M2.5 はどのプログラミング言語に対応していますか？

M2.5 は Python、JavaScript、TypeScript、Java、C++、Go、Rust、PHP、Ruby、Swift を含む **10 以上のプログラミング言語**をサポートし、特に Python と JavaScript で優れた性能を発揮します。

### M2.5 は AI エージェント構築に適していますか？

非常に適しています。M2.5 は**関数呼び出し**、**マルチステップ計画**、**Web ブラウジング**（BrowseComp 76.3%）で優れた性能を発揮します。その低コストを考慮すると、エージェントワークフローに最も適したモデルの一つです。

### MiniMax M3 とは何ですか？

M3 は MiniMax の次世代モデルで、CEO が **2026 年上半期**にリリースすることを確認しています。マルチモーダル機能と MoE アーキテクチャのさらなる改善が期待されています。M2.7 は初期の M3 イノベーションを取り入れたブリッジリリースとなる可能性があります。

## コントリビューション

コントリビューションを歓迎します！以下のガイドラインに従ってください：

1. このリポジトリを **Fork**
2. コントリビューション用の**新しいブランチ**を作成
3. 明確な説明を添えて **Pull Request** を提出
4. [Awesome list ガイドライン](https://github.com/sindresorhus/awesome/blob/main/contributing.md)に従っていることを確認

---

## 最新情報を入手

- **Star** でこのリポジトリをフォローして M2.7 と M3 の更新を受け取る
- **Watch** でリリース通知を受け取る
- [MiniMax](https://www.minimaxi.com) を**フォロー**して公式発表を確認

---

**MiniMax M2.5 を試す準備はできましたか？** [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) で始めましょう — OpenAI 互換 API で MiniMax モデルに最もお手頃にアクセスできます。

[![Atlas Cloud で始める](https://img.shields.io/badge/始める-Atlas_Cloud-green?style=for-the-badge&logo=cloud)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)
