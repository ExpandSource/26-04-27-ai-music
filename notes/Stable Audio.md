---
term: "Stable Audio"
aliases: [Stable Audio, Stability Audio]
tags: [ai, audio-generation, stability-ai, diffusion, generative-model]
created: "2026-04-25"
complexity: intermediate
domain: artificial-intelligence
---

# Stable Audio

> [!summary]
> Stable Audio는 Stability AI가 2023년부터 공개한 텍스트→오디오 생성 모델이다. 이미지 생성의 [[Stable Diffusion]] 접근을 오디오에 이식한 것으로, **Latent Diffusion**을 [[Mel-spectrogram]] 또는 압축 오디오 표현 위에서 수행한다.

## 핵심 개념

- **Latent Diffusion 기반**: 오디오를 잠재 표현으로 압축 → 그 위에서 디퓨전 → 디코더로 파형 복원.
- **버전**:
  - **Stable Audio 1.0** (2023): 텍스트 프롬프트로 효과음·짧은 음악 생성
  - **Stable Audio 2.0** (2024): 길이 확장(3분), 오디오→오디오 변환
  - 이후 오픈소스 가중치 일부 공개 (`stable-audio-open`)
- **강점**: 효과음(SFX)·앰비언트 사운드에 특히 강함. 짧은 클립 빠른 생성.
- **약점**: 보컬·가사 약함. [[Suno]]만큼의 "노래" 생성은 어려움.

## 상세 설명

Stable Audio는 [[Stable Diffusion]]의 성공 공식을 오디오에 적용한 사례로, "이미지에서 통한 디퓨전이 오디오에서도 통하는가?"라는 질문에 긍정적으로 답했다. 다만 음악·노래 영역에서는 자기회귀 토큰 예측 계열([[MusicGen]]·[[Suno]])이 더 유리하다는 평가가 굳어지고 있다.

Stability AI의 일부 모델 가중치 공개로 연구·개인 프로젝트에 활용되며, [[ComfyUI]]에서 오디오 노드 형태로도 사용된다. 강의 맥락에서는 "디퓨전이 음악 영역에서 어떻게 쓰였는지"의 사례로 짚는다.

## 예시

- 프롬프트: "ambient drone with rain sounds, 30 seconds" → 효과음 BGM
- 오디오→오디오: 기존 음원 → 비슷한 스타일의 변주
- 영상 효과음 제작용 짧은 클립 다수 생성

## 관련 개념

[[MusicLM]] · [[MusicGen]] · [[Suno]] · [[Mel-spectrogram]]
