---
term: "MusicGen"
aliases: [MusicGen, Meta MusicGen, AudioCraft]
tags: [ai, music-generation, meta, open-source, generative-model]
created: "2026-04-25"
complexity: intermediate
domain: artificial-intelligence
---

# MusicGen (Meta)

> [!summary]
> MusicGen은 Meta가 2023년 공개한 오픈소스 텍스트→음악 생성 모델이다. **단일 Transformer 구조**만으로 경쟁력 있는 음악을 생성하며, 코드와 가중치가 공개되어 있어 연구·개인 프로젝트의 표준 베이스라인이 됐다.

## 핵심 개념

- **구조**: 단일 자기회귀 Transformer + EnCodec 오디오 토크나이저. 복잡한 다단계 파이프라인 없이 하나의 모델로 처리.
- **생성 방식**: 오디오를 EnCodec으로 토큰화 → "다음 오디오 토큰" 예측 → EnCodec 디코더로 파형 복원.
- **강점**: 오픈소스. 로컬 GPU에서 실행 가능. 연구·파인튜닝의 표준.
- **약점**: 보컬 약함. 곡 길이 제한(15-30초). 일반 사용자용 UI 없음.
- **AudioCraft 일부**: Meta는 MusicGen을 AudioCraft 프레임워크의 일부로 공개. AudioGen·EnCodec과 함께 묶임.

## 상세 설명

MusicGen은 [[Suno]]·[[Udio]]가 따랐을 것으로 추정되는 **오디오 토큰 자기회귀** 접근의 공개 레퍼런스다. 텍스트 인코더(T5 계열)가 프롬프트를 임베딩하고, 자기회귀 Transformer가 EnCodec 토큰 시퀀스를 한 번에 하나씩 예측한다.

학계·개인 개발자에게는 [[Stable Diffusion]]이 이미지에서 했던 역할을 음악에서 한 모델이다. Hugging Face에 데모가 있어 가입 없이 체험 가능하나, 일반 사용자가 "한 곡 만들기" 용도로 쓰기엔 길이·UI 한계가 있다.

강의 맥락에서는 "Suno와 Lyria 뒤에 어떤 연구가 있는지"를 설명할 때 가장 명확한 레퍼런스가 된다.

## 예시

- "lo-fi hip-hop with drums and piano" → 15초 클립
- 멜로디 컨디셔닝: 허밍·기존 음원 일부 → 그 멜로디 기반 변주
- 연구자가 자신의 데이터셋으로 파인튜닝하여 특정 장르 특화 모델 제작

## 관련 개념

[[AudioLM]] · [[MusicLM]] · [[Stable Audio]] · [[Suno]] · [[Udio]]
