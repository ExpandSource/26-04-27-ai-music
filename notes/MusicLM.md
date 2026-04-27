---
term: "MusicLM"
aliases: [MusicLM, Music Language Model]
tags: [ai, music-generation, google, research, generative-model]
created: "2026-04-25"
complexity: advanced
domain: artificial-intelligence
---

# MusicLM

> [!summary]
> MusicLM은 Google이 2023년 발표한 텍스트→음악 생성 연구로, [[AudioLM]]의 접근을 음악에 적용했다. "차분한 바이올린 멜로디에 디스토션 기타가 깔린" 같은 긴 텍스트 프롬프트에서 5분짜리 음악을 생성할 수 있음을 보였다.

## 핵심 개념

- **계층적 토큰 예측**: [[AudioLM]]의 semantic + acoustic 토큰 구조를 음악에 확장.
- **MuLan 임베딩**: 음악과 텍스트를 같은 공간에 매핑한 사전학습 모델로 프롬프트와 음악 정렬.
- **긴 곡 생성**: 짧은 클립이 아닌 **수분 길이**의 일관된 음악 생성 가능.
- **공개 형태**: 논문 + 데모 사이트. 모델 가중치는 비공개 → 일반 사용자는 직접 못 씀.
- **후속 영향**: Google [[Google Lyria 3]]의 직접적 기반 기술.

## 상세 설명

2023년 1월 발표 당시 MusicLM은 "텍스트로 음악을 만든다"는 가능성을 학계에 각인시킨 첫 대형 시연이었다. 이전까지 AI 음악은 짧은 클립이나 특정 장르에 국한됐는데, MusicLM은 **다양한 장르 + 자유로운 텍스트 프롬프트 + 긴 곡 길이**의 세 축을 한 번에 처리했다.

직접 제품화되진 않았지만, 그 위에 Google이 [[Google Lyria 3]]을 만들어 Gemini 앱에 통합했다. Suno·Udio 같은 상업 서비스도 비슷한 아이디어를 자체 구현해 발전시킨 것으로 추정된다.

강의 맥락에서는 "AI 음악의 빅뱅 모멘트"를 짚을 때 가장 명확한 시점이다.

## 예시

- 프롬프트: "The main soundtrack of an arcade game. It is fast-paced and upbeat, with a catchy electric guitar riff..."
- 5분 길이 음악 생성 가능 (당시 데모 기준)
- 휘파람·허밍 → 그 멜로디 기반 풀 곡 변환

## 관련 개념

[[AudioLM]] · [[Google Lyria 3]] · [[MusicGen]] · [[Stable Audio]]
