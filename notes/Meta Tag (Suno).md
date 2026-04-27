---
term: "Meta Tag (Suno)"
aliases: [메타 태그, Suno Meta Tags, 곡 구조 태그]
tags: [ai, music-generation, suno, prompt-engineering]
created: "2026-04-25"
complexity: beginner
domain: artificial-intelligence
---

# Meta Tag (Suno)

> [!summary]
> Meta Tag는 [[Suno]] 가사 입력란에 **`[verse]` `[chorus]` `[bridge]` 같은 대괄호 표기**로 곡 구조를 직접 지시하는 표기다. 이 태그를 쓰면 모델이 "여기는 후렴", "여기는 변화 구간"을 명확히 인식해 곡 구조가 안정된다.

## 핵심 개념

- **자주 쓰는 구조 태그**:
  - `[intro]` — 도입부 (기악 중심)
  - `[verse]` `[verse 1]` `[verse 2]` — 벌스
  - `[pre-chorus]` — 후렴 직전 상승
  - `[chorus]` — 후렴 (가장 인상적)
  - `[bridge]` — 변화 구간 (한 번만)
  - `[solo]` — 악기 솔로
  - `[instrumental break]` — 기악 삽입
  - `[outro]` `[end]` — 마무리
- **보컬 스타일 태그**:
  - `[whispered]` — 속삭임
  - `[shouted]` — 외침
  - `[spoken]` — 말하기
- **무가사 지시**:
  - `[instrumental]` — 가사 없는 곡

## 상세 설명

Meta Tag는 Suno의 가장 강력한 제어 도구 중 하나다. 가사만 줄줄이 입력하면 모델이 임의로 구조를 만들지만, 태그를 명시하면 의도한 구조가 안정적으로 나온다. 특히 후렴이 약하게 나올 때 `[chorus]` 태그 + 짧은 가사 1-2줄로 압축하면 후렴이 도드라진다.

한국어 가사를 쓸 때도 메타 태그는 **영어로** 입력한다. 가사는 한국어, 태그는 영어인 조합이 가장 안정적.

영상 BGM·발표 인트로용 기악곡을 만들 때는 `[intro]` `[build-up]` `[climax]` `[outro]` 같은 흐름 태그가 유용하다. Suno가 모든 태그를 정확히 이해하지는 않지만, 일반적인 음악 용어 대부분이 작동한다.

## 예시

```
[verse]
오늘도 천천히 걸어가네

[chorus]
봄빛처럼 번져가네

[bridge]
그 순간 나는 알았지

[outro]
```

또는 무가사:

```
[intro]
[instrumental]
[verse]
[chorus]
[outro]
```

## 관련 개념

[[Suno]] · [[Instrumental]] · [[Extend (Suno)]]
