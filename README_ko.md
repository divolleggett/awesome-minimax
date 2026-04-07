# Awesome MiniMax M2 시리즈

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![MiniMax](https://img.shields.io/badge/MiniMax-M2_Series-blue?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZD0iTTEyIDJMMiAxOWgyMEwxMiAyeiIgZmlsbD0iI2ZmZiIvPjwvc3ZnPg==)](https://www.minimaxi.com)
[![Atlas Cloud](https://img.shields.io/badge/Atlas_Cloud-지금_시작-green?logo=cloud)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/divolleggett/awesome-minimax/pulls)

[English](README.md) | [中文](README_zh.md) | [日本語](README_ja.md) | **[한국어](README_ko.md)**

---

> **MiniMax M2.7이 곧 출시될 예정입니다! 이 페이지에서 M2 시리즈의 모든 정보를 추적합니다.**

---

**MiniMax M2 시리즈** 대규모 언어 모델과 관련된 리소스, 벤치마크, 도구, 커뮤니티 프로젝트를 엄선한 목록입니다. M2, M2.1, M2.5 및 곧 출시될 M2.7을 다룹니다.

## 목차

- [MiniMax M2란?](#minimax-m2란)
- [M2 시리즈 진화](#m2-시리즈-진화)
- [핵심 기능](#핵심-기능)
- [성능 벤치마크](#성능-벤치마크)
- [M2.7 전망](#m27-전망)
- [Atlas Cloud에서 MiniMax 체험](#atlas-cloud에서-minimax-체험)
- [API 빠른 시작](#api-빠른-시작)
- [가격](#가격)
- [M3 로드맵](#m3-로드맵)
- [커뮤니티 리소스](#커뮤니티-리소스)
- [자주 묻는 질문](#자주-묻는-질문)
- [기여하기](#기여하기)

## MiniMax M2란?

MiniMax M2는 **Mixture-of-Experts(MoE) 아키텍처** 기반의 오픈소스 대규모 언어 모델 제품군입니다. M2 시리즈는 **총 2,300억 개의 파라미터**를 보유하면서 추론 시 **100억 개의 파라미터만 활성화**하여, 극히 낮은 컴퓨팅 비용으로 최첨단 수준의 성능을 제공합니다.

주요 아키텍처 특징:

- **MoE 설계** — 2,300억 총/100억 활성 파라미터로 고품질 출력과 낮은 지연 시간 실현
- **오픈소스** — Apache 2.0 라이선스로 공개, 상업적 사용 완전 지원
- **긴 컨텍스트** — 복잡한 추론 작업을 위한 확장 컨텍스트 윈도우 지원
- **다국어 지원** — 영어, 중국어, 일본어, 한국어 등 다양한 언어에서 뛰어난 성능
- **코드 네이티브** — 10개 이상의 프로그래밍 언어에 대한 코딩 작업에 특화된 학습

M2 시리즈는 여러 차례의 반복을 통해 빠르게 발전하여, 각 버전에서 속도, 코딩 능력, 에이전트 기능이 크게 향상되었습니다.

## M2 시리즈 진화

| 버전 | 출시일 | 주요 특징 | 라이선스 |
|------|-------|----------|---------|
| **M2** | 2025년 10월 | 첫 오픈소스 릴리스. MoE 아키텍처, 2,300억/100억 파라미터. 추론, 코딩, 다국어 작업에서 강력한 기준선. | Apache 2.0 |
| **M2.1** | 2025년 12월 | 다국어 지원 강화. 코딩 능력 개선. 지시 따르기 향상 및 환각 감소. | Apache 2.0 |
| **M2.5** | 2026년 2월 | SWE-Bench 80.2%, BrowseComp 76.3%. M2 대비 37% 빠른 추론. 최첨단 에이전트 및 도구 호출 성능. | Apache 2.0 |
| **M2.7** | 곧 출시 | M2 발전 궤적에 기반한 개선 예상. 속도와 기능의 추가 향상 기대. | 미정 |

## 핵심 기능

### 뛰어난 코딩 능력

MiniMax M2.5는 Python, JavaScript, TypeScript, Java, C++, Go, Rust, PHP, Ruby, Swift를 포함한 **10개 이상의 프로그래밍 언어**에서 탁월한 성능을 발휘합니다.

- **SWE-Bench Verified**: 80.2% — 실제 GitHub 이슈를 자율적으로 해결
- **Multi-SWE-Bench**: 51.3% — 멀티 리포지토리 코드베이스 처리
- **HumanEval+**: 코드 생성 작업에서 높은 합격률
- **코드 리뷰 및 리팩터링** — 복잡한 코드베이스를 이해하고 개선 사항 제안

### 에이전트 및 도구 호출

M2.5는 에이전트 워크플로우를 위해 설계되었습니다:

- **네이티브 함수 호출** — JSON 스키마 지원을 통한 구조화된 도구 사용
- **다단계 계획** — 복잡한 작업을 실행 가능한 단계로 분해
- **웹 브라우징** — BrowseComp 76.3%로 강력한 웹 내비게이션 능력 입증
- **API 오케스트레이션** — 여러 API 호출을 연쇄하여 작업 완료

### 추론 및 계획

- **사고의 연쇄 추론** — 수학 및 논리 벤치마크에서 우수한 성능
- **긴 컨텍스트 이해** — 긴 문서의 처리 및 추론
- **작업 분해** — 복잡한 문제를 관리 가능한 하위 작업으로 분할

## 성능 벤치마크

**MiniMax M2.5**(현재 최신 안정 버전)의 성능 데이터:

| 벤치마크 | 점수 | 카테고리 |
|---------|------|---------|
| SWE-Bench Verified | **80.2%** | 소프트웨어 엔지니어링 |
| Multi-SWE-Bench | **51.3%** | 멀티 리포 엔지니어링 |
| BrowseComp | **76.3%** | 웹 브라우징 및 내비게이션 |
| 추론 속도 | **100 tokens/sec** (네이티브) | 처리량 |

### 버전별 속도 개선

| 버전 | 상대 속도 | 비고 |
|------|----------|------|
| M2 | 1.0x (기준) | 초기 릴리스 |
| M2.1 | ~1.15x | 소폭 최적화 |
| M2.5 | **1.37x** | M2 대비 37% 빠름 |
| M2.7 | 미정 | 추가 개선 예상 |

## M2.7 전망

MiniMax는 아직 M2.7의 사양을 공식 발표하지 않았지만, M2 시리즈의 발전 궤적을 바탕으로 합리적인 예측이 가능합니다:

### 발전 패턴

M2 시리즈의 각 버전은 측정 가능한 개선을 가져왔습니다:

- **M2 → M2.1**: 다국어 지원 향상, 코딩 개선, 환각 감소
- **M2.1 → M2.5**: 벤치마크 대폭 향상(SWE-Bench 80.2%), 37% 속도 향상, 에이전트 기능
- **M2.5 → M2.7**: 이러한 상승 추세의 지속 예상

### 예상되는 개선 사항

확립된 패턴과 MiniMax CEO의 공개 발언에 기반:

1. **추가 속도 향상** — 각 반복마다 더 빨라짐. M2.7은 네이티브로 130+ tokens/sec를 넘을 가능성.
2. **더 강력한 코딩 벤치마크** — SWE-Bench 점수가 꾸준히 상승. M2.7은 SWE-Bench Verified에서 83%+ 목표 가능.
3. **강화된 에이전트 기능** — 도구 호출과 다단계 계획은 MiniMax의 핵심 분야.
4. **더 나은 추론 능력** — 개선된 사고의 연쇄 및 수학적 추론.
5. **M3로의 다리** — MiniMax CEO가 M3를 2026년 상반기에 확인. M2.7은 M3를 위한 주요 아키텍처 개선을 통합한 브릿지 릴리스일 가능성.

> **M2.7은 출시 시 [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)에서 이용할 수 있습니다.** 세부 사항이 발표되는 대로 이 페이지를 업데이트하겠습니다.

## Atlas Cloud에서 MiniMax 체험

[Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)는 OpenAI 호환 API를 통해 MiniMax M2 시리즈 모델에 대한 빠르고 저렴한 액세스를 제공합니다.

**Atlas Cloud를 선택하는 이유:**

- **최저 가격** — M2.5는 백만 토큰당 $0.27 / $0.95 (입력/출력)
- **OpenAI 호환 API** — GPT나 Claude에서 코드 한 줄만 변경하여 전환
- **높은 처리량** — 빠른 추론을 위해 최적화된 인프라
- **유료 플랜 속도 제한 없음** — 제한 없이 확장
- **모든 M2 버전 이용 가능** — M2, M2.1, M2.5에 지금 바로 액세스

[![Atlas Cloud에서 체험](https://img.shields.io/badge/MiniMax_체험-Atlas_Cloud-green?style=for-the-badge&logo=cloud)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)

## API 빠른 시작

Atlas Cloud의 MiniMax는 **OpenAI 호환 API**를 사용하여 통합이 쉽습니다.

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
        {"role": "system", "content": "당신은 도움이 되는 코딩 어시스턴트입니다."},
        {"role": "user", "content": "에라토스테네스의 체를 사용하여 n 이하의 모든 소수를 찾는 Python 함수를 작성하세요."}
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
      {"role": "system", "content": "당신은 도움이 되는 코딩 어시스턴트입니다."},
      {"role": "user", "content": "JavaScript에서 async/await와 Promise의 차이점을 설명하세요."}
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
    { role: "system", content: "당신은 도움이 되는 코딩 어시스턴트입니다." },
    { role: "user", content: "Express.js로 입력 유효성 검사가 포함된 REST API 엔드포인트를 만드세요." },
  ],
  temperature: 0.7,
  max_tokens: 2048,
});

console.log(response.choices[0].message.content);
```

## 가격

MiniMax M2.5의 가장 큰 장점 중 하나는 **뛰어난 가성비**입니다. MoE 아키텍처(2,300억 총 파라미터 중 100억만 활성) 덕분에 추론 비용이 비슷한 모델에 비해 극적으로 낮습니다.

| 모델 | 입력 (백만 토큰당) | 출력 (백만 토큰당) | 아키텍처 |
|------|-------------------|-------------------|---------|
| **MiniMax M2.5** | **$0.27** | **$0.95** | MoE 2,300억/100억 |
| GPT-4o | $2.50 | $10.00 | Dense |
| Claude 3.5 Sonnet | $3.00 | $15.00 | Dense |
| DeepSeek V3 | $0.27 | $1.10 | MoE |

> MiniMax M2.5는 최첨단 수준의 코딩 성능을 GPT-4o 및 Claude 3.5 Sonnet보다 **최대 90% 저렴**하게 제공합니다.

**[Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)에서 최고의 MiniMax 가격으로 시작하세요.**

## M3 로드맵

MiniMax CEO는 **M3를 2026년 상반기에 출시할 계획**임을 확인했습니다. 현재 알려진 사항:

- **멀티모달 융합** — M3는 텍스트, 이미지, 오디오, 비디오 모달리티의 네이티브 지원 예상
- **더 높은 효율성** — 비용 대비 성능 비율 향상을 위한 MoE 아키텍처 지속 개선
- **더 강력한 추론** — 복잡한 추론 벤치마크에서 차세대 수준의 성능 목표
- **M2.7이 다리 역할** — M2.7은 초기 M3 혁신을 통합하여 가교 역할을 할 가능성

더 많은 세부 사항이 공개되면 이 섹션을 업데이트하겠습니다. 최신 정보를 받으려면 Star를 눌러주세요!

## 커뮤니티 리소스

### 공식 리소스

- [MiniMax 공식 웹사이트](https://www.minimaxi.com) — 공식 회사 페이지
- [MiniMax 하이루오 AI](https://hailuoai.com) — MiniMax 소비자 AI 제품
- [MiniMax API 문서](https://www.minimaxi.com/document/introduction) — 공식 API 문서
- [MiniMax on Hugging Face](https://huggingface.co/MiniMaxAI) — 모델 가중치 및 데모

### 기술 논문 및 글

- [MiniMax-01 기술 보고서](https://arxiv.org/abs/2501.08313) — 원본 아키텍처 논문
- [M2 시리즈 기술 보고서](https://www.minimaxi.com/news/minimax-m2-series) — 공식 M2 시리즈 세부 정보

### 커뮤니티 프로젝트

- [MiniMax Cookbook](https://github.com/MiniMax-AI) — 공식 예제 및 튜토리얼
- [Awesome LLM](https://github.com/Hannibal046/Awesome-LLM) — 포괄적인 LLM 리소스 목록

### 도구 및 통합

- [LiteLLM](https://github.com/BerriAI/litellm) — MiniMax를 포함한 100+ LLM의 통합 API
- [OpenRouter](https://openrouter.ai/) — 멀티 모델 API 게이트웨이
- [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax) — 저렴한 MiniMax API 액세스

## 자주 묻는 질문

### MiniMax M2가 다른 LLM과 다른 점은 무엇인가요?

MiniMax M2는 **Mixture-of-Experts(MoE) 아키텍처**를 사용하며, 총 2,300억 개의 파라미터 중 추론 시 100억 개만 활성화됩니다. 100억 모델을 실행하는 비용으로 2,300억 모델의 품질을 얻을 수 있습니다. Apache 2.0 라이선스와 강력한 코딩 벤치마크를 결합하면, 가장 가성비가 좋은 최첨단 모델 중 하나입니다.

### MiniMax M2는 오픈소스인가요?

네. MiniMax M2, M2.1, M2.5는 모두 **Apache 2.0 라이선스**로 출시되어 상업적 사용, 수정, 재배포가 가능합니다.

### M2.5의 코딩 능력은 GPT-4o와 비교해 어떤가요?

M2.5는 **SWE-Bench Verified에서 80.2%**를 달성하여, 실제 소프트웨어 엔지니어링 작업에서 GPT-4o와 동등하거나 이를 초과합니다. 백만 토큰당 $0.27/$0.95로 동등한 코딩 품질이 **약 10분의 1 가격**에 가능합니다.

### M2.7은 언제 출시되나요?

공식 출시일은 아직 발표되지 않았습니다. 이전 출시 간격(2025년 10월, 12월, 2026년 2월)으로 볼 때, M2.7은 **2026년 2분기**에 나올 가능성이 있습니다. 공식 정보가 나오는 대로 이 페이지를 업데이트하겠습니다.

### 기존 OpenAI 코드로 MiniMax M2를 사용할 수 있나요?

네! [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)를 통해 MiniMax M2는 **OpenAI 호환 API**로 이용할 수 있습니다. `base_url`과 `api_key`만 변경하면 기존 코드가 그대로 작동합니다.

### M2.5는 어떤 프로그래밍 언어를 지원하나요?

M2.5는 Python, JavaScript, TypeScript, Java, C++, Go, Rust, PHP, Ruby, Swift를 포함한 **10개 이상의 프로그래밍 언어**를 지원하며, 특히 Python과 JavaScript에서 뛰어난 성능을 보입니다.

### M2.5는 AI 에이전트 구축에 적합한가요?

매우 적합합니다. M2.5는 **함수 호출**, **다단계 계획**, **웹 브라우징**(BrowseComp 76.3%)에서 뛰어난 성능을 발휘합니다. 낮은 비용을 고려하면 에이전트 워크플로우에 가장 적합한 모델 중 하나입니다.

### MiniMax M3는 무엇인가요?

M3는 MiniMax의 차세대 모델로, CEO가 **2026년 상반기** 출시를 확인했습니다. 멀티모달 기능과 MoE 아키텍처의 추가 개선이 예상됩니다. M2.7은 초기 M3 혁신을 통합한 브릿지 릴리스일 가능성이 있습니다.

## 기여하기

기여를 환영합니다! 다음 가이드라인을 따라주세요:

1. 이 리포지토리를 **Fork**
2. 기여를 위한 **새 브랜치** 생성
3. 명확한 설명과 함께 **Pull Request** 제출
4. [Awesome list 가이드라인](https://github.com/sindresorhus/awesome/blob/main/contributing.md)을 따르고 있는지 확인

---

## 최신 정보 받기

- **Star**를 눌러 M2.7 및 M3 업데이트 알림 받기
- **Watch**로 릴리스 알림 받기
- [MiniMax](https://www.minimaxi.com)를 **팔로우**하여 공식 발표 확인

---

**MiniMax M2.5를 시작할 준비가 되셨나요?** [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)에서 시작하세요 — OpenAI 호환 API로 MiniMax 모델에 가장 저렴하게 액세스할 수 있습니다.

[![Atlas Cloud에서 시작](https://img.shields.io/badge/시작하기-Atlas_Cloud-green?style=for-the-badge&logo=cloud)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-minimax)
