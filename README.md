# 26-04-27 · AI를 활용한 나만의 음악 및 음원 작곡하기

2026년 월요 AI 강의 시리즈 **3회차** (2026-04-27, 14:00-16:00).
대상 청중: 40-60대, 1·2회차(생성형 AI · AI 이미지) 참석 경험.

## 구조

| 파일 | 역할 |
|---|---|
| `lecture.md` | One Source. 책 형태의 풍성한 글. Pandoc article-html/pdf 렌더 대상. |
| `slides.md` | 발표용 Slidev 슬라이드 (파생). |
| `labs.md` | 실습 워크북 (Suno 무료 크레딧 30분 블록). |
| `notes/` | Obsidian 호환 용어 노트 (Suno · Lyria · 음악 기술). |
| `public/images/` | UI 스크린샷 placeholder. `{섹션}-{slug}.png`. |
| `public/audio/` | Suno · Gemini 생성 오디오 샘플 placeholder. `{섹션}-{slug}.mp3`. |
| `assets/` | Ref.md 등 강의 외 참고자료. |

## 실행

```bash
bun install              # 최초 1회
bun run dev              # http://localhost:3030 발표 미리보기
bun run build            # dist/ 정적 SPA
bun run export           # slides-export.pdf (Playwright 필요)
```

배포용 빌드 (GitHub Pages):

```bash
bun run build -- --base /26-04-27-ai-music/
```

Pandoc article 렌더 (모노레포 루트):

```bash
make article-html LECTURE=lectures/26-04-27-ai-music
make article-pdf  LECTURE=lectures/26-04-27-ai-music
make slidev-pdf   LECTURE=lectures/26-04-27-ai-music
```

## 이미지 · 오디오 Placeholder 규약

**이미지** — `public/images/`에 `{섹션번호}-{내용-slug}.png`.
강사가 강의 당일 Suno · Gemini UI 스크린샷으로 채움.

**오디오** — `public/audio/`에 `{섹션번호}-{내용-slug}.mp3`.
강사가 Suno · Gemini 생성 결과물로 채움.
slides.md에서 `<audio controls src="/audio/..."></audio>`로 embed.
