---
term: "Google Lyria 3"
aliases: [Lyria, Lyria 3, Gemini Music, Lyria RealTime]
tags: [ai, music-generation, google, gemini, generative-model]
created: "2026-04-25"
complexity: beginner
domain: artificial-intelligence
---

# Google Lyria 3

> [!summary]
> Lyria는 Google DeepMind의 음악 생성 모델 라인이다. **Lyria 3**(2025)는 Gemini 앱에 **Tools → Create music**으로 통합되어 일반 사용자가 직접 사용할 수 있게 됐다. 무료 Fast 모델은 30초 트랙, Thinking·Pro 티어는 풀 트랙을 만든다.

## 핵심 개념

- **계보**: [[AudioLM]](2022) → [[MusicLM]](2023) → Lyria 1/2(2024) → **Lyria 3**(2025).
- **티어별 길이**:
  - **Fast**: 30초 (무료 사용자 기본)
  - **Thinking / Pro**: 풀 트랙 (수분, 유료/고급 사용자)
- **접근 경로**: gemini.google.com → 입력창 옆 **Tools** → **Create music**.
- **강점**: Gemini 통합 — 한 인터페이스에서 텍스트·이미지·음악까지 자연스럽게.
- **약점**: 무료 길이 제한(30초)으로 "한 곡" 만들기엔 부족. 보컬·가사 영역은 [[Suno]] 대비 약함.

## 상세 설명

Lyria의 기반은 Google DeepMind의 [[MusicLM]]이다. 음악을 **오디오 토큰**으로 쪼개 자기회귀 방식으로 다음 토큰을 예측하는 언어 모델 접근. 2024년 YouTube Shorts·Vids·일부 파트너에 우선 제공됐고, 2025년 일반 Gemini 사용자에게 공개됐다.

음악 강의 맥락에서 Lyria 3은 **"입문 체험"** 도구로 적합하다. 1·2회차에서 익숙해진 Gemini 안에서 "AI가 음악도 만든다"는 감을 빠르게 잡고, 그 한계가 자연스럽게 [[Suno]] V4.5로의 전환을 이끈다. 본격적인 한 곡 제작은 무료 환경에서는 [[Suno]]가 적합하다.

비가청 워터마크 [[SynthID]]가 Lyria 생성물에 기본 삽입되어 있어, AI 생성 여부를 기술적으로 식별할 수 있다.

## 예시

- "잔잔한 피아노 중심의 봄 산책 배경음악" → Fast 30초 트랙
- "카페 분위기의 로파이 힙합" → Fast 30초 샘플
- Thinking 모드: "K-pop ballad, female vocal, sad" → 풀 트랙 (유료)

## 관련 개념

[[Suno]] · [[MusicLM]] · [[AudioLM]] · [[MusicGen]]
