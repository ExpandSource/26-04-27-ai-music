---
term: "AudioLM"
aliases: [AudioLM, Audio Language Model]
tags: [ai, audio-generation, google, research, generative-model]
created: "2026-04-25"
complexity: advanced
domain: artificial-intelligence
---

# AudioLM

> [!summary]
> AudioLM은 Google이 2022년 발표한 연구로, **오디오를 언어 모델처럼** 다루는 접근의 시작점이다. 음성·음악을 토큰 시퀀스로 쪼개 "다음 토큰"을 예측함으로써 길고 일관된 오디오를 생성할 수 있음을 증명했다.

## 핵심 개념

- **핵심 아이디어**: 오디오를 **이산 토큰**으로 변환 → 언어 모델(Transformer)로 다음 토큰 예측 → 다시 파형으로 복원.
- **두 단계 토큰**:
  - **Semantic tokens**: 의미·구조(음운·멜로디 윤곽) 담당
  - **Acoustic tokens**: 음색·소리 디테일 담당
  - 두 단계를 계층적으로 예측해 긴 오디오의 일관성 확보.
- **결과**: 짧은 오디오 입력만으로 길고 자연스러운 연속 오디오 생성. 문법 없이 음운 학습 → 발음·억양 자연.

## 상세 설명

AudioLM은 직접 사용 가능한 제품은 아니지만, 이후 모든 음악·음성 생성 모델의 **기반 아이디어**가 됐다. [[MusicLM]]은 AudioLM의 음악 버전, [[Google Lyria 3]]은 그 직계 후손이다. [[Suno]]·[[Udio]]·[[MusicGen]]도 모두 "오디오 토큰 자기회귀" 접근을 공유한다.

음악 강의 맥락에서는 "Suno가 어떻게 한 줄 프롬프트로 한 곡을 만드는가?"라는 질문의 출발점이다. 텍스트 LLM이 단어 단위로 글을 짓듯, AudioLM의 후예들은 오디오 토큰 단위로 곡을 짓는다.

## 예시

- 짧은 음성 한 마디 입력 → 같은 화자의 자연스러운 연속 발화 생성 (음성 영역)
- 짧은 피아노 연주 입력 → 그 스타일을 이어가는 긴 음악 (음악 영역, [[MusicLM]]에서 확장)

## 관련 개념

[[MusicLM]] · [[Google Lyria 3]] · [[MusicGen]] · [[Suno]]
