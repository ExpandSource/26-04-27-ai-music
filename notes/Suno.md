---
term: "Suno"
aliases: [수노, Suno AI, Suno V4.5]
tags: [ai, music-generation, service, suno, generative-model]
created: "2026-04-25"
complexity: beginner
domain: artificial-intelligence
---

# Suno

> [!summary]
> Suno는 텍스트 프롬프트와 가사로부터 보컬과 반주가 어우러진 **완성형 곡**을 생성하는 음악 AI 서비스다. 무료 계정으로도 하루 50 [[Credit (Suno)]]을 받아 한 곡을 끝까지 만들 수 있어, 일반 사용자가 진입하기 가장 쉬운 음악 생성 도구로 자리잡았다.

## 핵심 개념

- **모델 라인업**: V1(2023) → V4(2024) → **V4.5(2025, 무료 전용)** → V5/V5.5(유료).
- **무료 모델 V4.5**: 무료 계정에서 쓸 수 있는 최상위. 최대 8분 곡 길이, 한국어 가사 발음 개선, 강력한 [[Cover (Suno)]]·[[Persona (Suno)]]·[[Extend (Suno)]].
- **인터페이스 8단계**: Explore → Create → Lyrics → Styles → More Options → Library → Remix → Publish.
- **크레딧 모델**: 한 곡 생성 ≈ 10 [[Credit (Suno)]]. 무료 50/일 갱신, 미사용 분 이월 안 됨.
- **메타 태그**: `[verse]` `[chorus]` `[bridge]` `[instrumental]` 등으로 곡 구조를 직접 지시 — [[Meta Tag (Suno)]].

## 상세 설명

Suno의 아키텍처는 공개되지 않았지만, [[MusicGen]]과 같은 **자기회귀형 오디오 토큰 예측** 계열에 [[Stable Audio]]의 디퓨전 기법을 결합한 하이브리드로 추정된다. 가장 큰 도약은 **보컬과 가사**를 자연스럽게 얹는 능력으로, 이전까지 "기악곡"에만 머물던 AI 음악 영역을 "노래"로 확장했다.

2024년 [[Udio]]와의 경쟁 구도가 형성됐고, 2025년 V4.5에서 한국어를 포함한 다국어 가사 발음이 크게 개선됐다. 강의·실습 환경에서는 **무료 계정만으로 한 곡 완결 경험**을 줄 수 있다는 점이 결정적이다.

## 예시

- 프롬프트: `Korean ballad, acoustic piano, female vocal` + 한국어 가사 4줄 → 2-3분짜리 발라드 곡 생성
- 같은 가사를 [[Cover (Suno)]]로 K-pop 장르로 재해석 → 분위기 완전 전환
- [[Extend (Suno)]]로 30초 인트로를 3분 풀 트랙으로 확장

## 관련 개념

[[Google Lyria 3]] · [[Udio]] · [[MusicGen]] · [[Persona (Suno)]] · [[Cover (Suno)]] · [[Extend (Suno)]] · [[Meta Tag (Suno)]] · [[Credit (Suno)]]
