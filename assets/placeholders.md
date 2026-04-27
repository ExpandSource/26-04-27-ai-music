# Placeholder · Source 목록 — 26-04-27 AI 음악

이 문서는 두 역할을 한다.

1. **작업 가이드** — 강사·작업자가 이미지·오디오 placeholder를 채울 때 어떤 도구로 어떤 결과물을 만들지 안내한다.
2. **Source 목록** — `lecture.md`·`slides.md`가 의존하는 외부 자산을 한눈에 파악한다. 누락 점검에도 사용.

---

## 진행 상황 (체크하면서 진행)

### 이미지 (총 15개)

**다이어그램·콜라주 (4)**
- [x] `0.0-cover-collage.png`
- [x] `1.1-text-image-music.png`
- [x] `1.3-tech-lineage.png`
- [x] `2.1-services-map.png`

**UI 스크린샷 (8)**
- [x] `3.2-gemini-create-music.png`
- [x] `4.1-suno-dashboard.png`
- [x] `4.3-suno-explore.png`
- [x] `4.4-suno-create-simple.png`
- [x] `4.4-suno-create-advanced.png` *(추가됨)*
- [x] `4.5-suno-lyrics.png`
- [x] `4.5-suno-lyrics-2.png` *(추가됨)*
- [x] `4.6-suno-styles.png`
- [x] `4.8-suno-library.png`

**결과 비교 (2)**
- [x] `4.9-suno-original.png`
- [x] `4.9-suno-remix.png`

### 오디오 — Suno 생성 mp3 (6)

- [x] `apricot-hammer.mp3` — warm piano instrumental → **5.1 Instrumental 레시피**
- [x] `spring-light-spreads.mp3` — 한국어 K-Pop 발라드, 봄 산책 → **5.2 한국어 발라드 레시피**
- [x] `saturday-stillness.mp3` — warm acoustic, 주말 아침 → **5.5 인디 어쿠스틱 + Persona 데모 (원본)**
- [x] `city-heart.mp3` — 같은 보컬, 90년대 한국 댄스 → **Persona 데모 (변형)**
- [x] `wet-afternoon.mp3` — ambient dream pop ballad → **보너스 레시피 + Cover 원본**
- [x] `wet-afternoon-x-apricot-hammer-mashup.mp3` — Cover/Mashup → **Cover 데모 (after)**
- [x] `patpat-waiting.mp3` — kids pop lullaby, 72 BPM → **보너스 레시피**
- [x] `turn-up-the-audio.mp3` — 메타적 마무리 → **엔딩 슬라이드 BGM**
- [x] `3.3-gemini-spring-walk.mp3` — Gemini Fast 30초 → **3.3 Gemini 맛보기**

### 비디오 — Gemini Lyria 생성 mp4 (앨범커버 + 오디오)

- [x] `speed-of-light-curiosity.mp3 / .mp4` — Gemini, "AI 학습자를 위한 경쾌한 곡" → **cover BGM + 오프닝 영상**
- [x] `our-new-blueprint.mp3 / .mp4` — Gemini, 영감·차분 → **마무리 직전 영상**
- [x] `nine-am-window-seat.mp4` — Gemini, 어쿠스틱 모닝 → **3.3 Gemini 결과 시연**
- [x] `table-by-the-window.mp4` — Gemini, 카페 로파이 → **3.3 Gemini 결과 시연**

---

## 이미지 — 카테고리 1. 다이어그램·콜라주 (AI 생성)

이미지 생성 AI(Midjourney·Nano Banana·Gemini Image)로 만든다. 16:9 가로 비율 권장. 본문 흐름과 어울리는 톤(파랑-보라 계열)으로 통일.

### `0.0-cover-collage.png` — 커버 이미지
- **사용**: `lecture.md` L27 (서문)
- **설명**: 이번 회차의 표지. 음악 AI의 분위기를 한 장에 담음.
- **권장 프롬프트**:
  ```
  Cover collage for AI music lecture: waveforms, music notes, headphones,
  microphone icons, abstract sound waves, blue-purple gradient background,
  modern minimalistic, 16:9
  ```
- **도구**: Midjourney `--ar 16:9` 또는 Nano Banana
- **slides.md 영향**: `styles/index.css`의 `.cover-image` 배경. cover 슬라이드 배경이 됨.

### `1.1-text-image-music.png` — 세 영역 비교 인포그래픽
- **사용**: `lecture.md` L49 (1.1 텍스트·이미지·음악 차이)
- **설명**: 텍스트·이미지·음악 세 영역을 가로로 나란히 비교한 인포그래픽.
- **권장 프롬프트**:
  ```
  Three-column comparison infographic: text generation, image generation,
  music generation. Each column with icon (document, picture, waveform)
  + brief input/output labels. Pastel tones, clean modern style, 16:9
  ```
- **대체**: Mermaid flowchart로 슬라이드 안에서 직접 그려도 됨.

### `1.3-tech-lineage.png` — 기술 계보 흐름도
- **사용**: `lecture.md` L93 (1.3 기술 계보)
- **설명**: AudioLM(2022) → MusicLM(2023) → Lyria 3 / Suno V4.5 (2025)의 시간 흐름.
- **권장 프롬프트**: AI 그림보다 **Mermaid가 정확**. 슬라이드는 이미 Mermaid 사용. lecture.md용으로만 정적 이미지가 필요하면:
  ```
  Timeline infographic of AI music model evolution from 2022 to 2025,
  showing AudioLM, MusicLM, MusicGen, Stable Audio, Lyria 3, Suno V4.5
  as connected nodes on a horizontal timeline, soft blue color scheme, 16:9
  ```

### `2.1-services-map.png` — 서비스 포지셔닝 맵
- **사용**: `lecture.md` L164 (2.1 서비스 개관)
- **설명**: 2축 맵. X축: 쉬움 ↔ 정교함 / Y축: 기악 중심 ↔ 보컬 중심.
- **배치할 서비스**: Gemini Lyria 3, Suno, Udio, MusicGen, Stable Audio, ElevenLabs Music
- **권장 프롬프트**:
  ```
  2-axis positioning map for AI music services. X-axis: simple to advanced.
  Y-axis: instrumental focus to vocal/song focus. Place service names as
  labeled dots: Gemini Lyria, Suno, Udio, MusicGen, Stable Audio. Clean
  white background, brand-neutral color dots, 16:9
  ```

---

## 이미지 — 카테고리 2. UI 스크린샷 (캡처)

Gemini와 Suno의 화면을 직접 캡처한다. **강의 당일 아침**(또는 며칠 전)에 캡처해야 최신 UI 반영. UI는 자주 바뀐다.

### 캡처 환경 권장
- 브라우저: Chrome 또는 Firefox, 윈도우 크기 1920×1080 이상
- 확대율: 100% (또는 125%까지)
- 다크모드 OFF (강의 자료는 라이트 모드 통일)
- 개인 정보 노출 부분(이메일·실명) 모자이크 처리

### `3.2-gemini-create-music.png` — Gemini Create music 진입
- **사용**: `lecture.md` L219 / `slides.md` L284 (3.2 Gemini 진입)
- **캡처**: gemini.google.com 접속 → 입력창 옆 **Tools(도구)** 메뉴 펼친 상태 → "Create music" 항목이 강조되도록.
- **참고**: image-right 레이아웃이라 세로/정사각형 비율도 OK.

### `4.1-suno-dashboard.png` — Suno 대시보드 (크레딧 표시)
- **사용**: `lecture.md` L279 (4.1 무료 크레딧 안내)
- **캡처**: suno.com 로그인 후 메인 대시보드. 좌측 네비(Home/Explore/Create/Library) + **우상단 크레딧 잔량 표시 강조**.

### `4.3-suno-explore.png` — Explore 탭
- **사용**: `lecture.md` L314 / `slides.md` L528 (4.3 Explore)
- **캡처**: Explore 페이지. 타일형 곡 카드 그리드 + 상단 장르 필터가 보이는 상태. 한국어 곡 카드가 일부 노출되면 좋음.

### `4.4-suno-create-simple.png` — Create Simple 모드
- **사용**: `lecture.md` L339 / `slides.md` L552 (4.4 Create)
- **캡처**: Create 화면 Simple 모드. 중앙 프롬프트 박스에 예시 텍스트(`80s synthpop, female vocal, dreamy`) 입력된 상태 + 하단 Generate 버튼.

### `4.5-suno-lyrics.png` — Custom 모드 Lyrics 박스
- **사용**: `lecture.md` L388 / `slides.md` L576 (4.5 Lyrics)
- **캡처**: Create 화면 Custom 모드. Lyrics 박스에 메타 태그가 섞인 한국어 가사 (`[verse]`/`[chorus]` 포함) 입력된 상태.

### `4.6-suno-styles.png` — Styles 패널
- **사용**: `lecture.md` L417 / `slides.md` L651 (4.6 Styles)
- **캡처**: Custom 모드의 Styles 박스. 영어 키워드(`80s synthpop, female vocal, dreamy, synth pads, drum machine`)가 입력된 상태.

### `4.8-suno-library.png` — Library 화면
- **사용**: `lecture.md` L449 / `slides.md` L715 (4.8 Library)
- **캡처**: Library 페이지. 생성된 곡들이 리스트로 쌓여있고 각 항목에 재생/다운로드/Remix 아이콘이 보이는 상태. 곡 제목 일부에 한국어 노출 권장.

---

## 이미지 — 카테고리 3. 결과 캡처 (Suno로 직접 만들기)

`compare` 레이아웃에서 Before/After를 보여주는 두 장.

### `4.9-suno-original.png` + `4.9-suno-remix.png` — Remix 비교
- **사용**: `slides.md` L739-740 (4.9 Remix·Extend·Cover, compare 레이아웃)
- **만드는 법**:
  1. Suno에서 한 곡 생성 (예: Lab 2의 한국어 발라드)
  2. 그 곡 → Library → **Remix** → 장르를 완전히 다른 것으로 (lofi 또는 K-pop)
  3. Library에서 두 곡(원본 + Remix)이 나란히 보이는 상태를 캡처 → 두 장으로 분할 또는 각각 곡 카드 캡처
- **권장 비율**: 같은 종횡비로 통일 (compare 레이아웃에서 좌·우 대칭)

---

## 오디오 — Suno·Gemini 생성 결과물

오디오는 모두 직접 생성. 길이는 30초~2분 권장 (강의 중 들려주기 적당). mp3 192kbps 이상.

### `3.3-gemini-spring-walk.mp3` — Gemini 30초 샘플
- **사용**: `slides.md` L373 (3.3 Gemini 맛보기)
- **도구**: Gemini Lyria 3 (Fast 모델, 무료)
- **프롬프트**:
  ```
  잔잔한 피아노 중심의 봄 산책 배경음악, 따뜻한 분위기
  ```
- **길이**: 30초 (Fast 모델 기본)
- **용도**: Gemini의 결과물을 그대로 들려줘 "이게 30초 한계"임을 체감시키는 용도.

### `5.2-lofi-rainy.mp3` — Suno Lofi 비 오는 날
- **사용**: `slides.md` L855 (레시피 1 — Lofi 배경음악)
- **도구**: Suno V4.5 무료
- **프롬프트** (Custom 모드):
  ```
  Styles: lofi hip-hop, chill, rainy day, piano, soft drums, no vocals,
  warm analog texture
  Lyrics: [instrumental]
  ```
- **길이**: 1분 정도 (긴 풀 트랙은 시간 낭비. 원본 1-2분, 강의 중 30초만 들려도 충분)
- **용도**: Instrumental 레시피의 결과 시연.

### `5.2-korean-ballad.mp3` — 한국어 발라드
- **사용**: `slides.md` L900 (레시피 2 — 한국어 발라드)
- **도구**: Suno V4.5 무료
- **프롬프트** (Custom 모드):
  ```
  Styles: Korean ballad, acoustic piano, strings, female vocal, tender, nostalgic
  Lyrics:
  [verse]
  햇살이 머물던 그 식탁 위
  엄마의 손길이 스며있던 밥

  [chorus]
  오래된 노래처럼
  천천히 번져가는 이 마음
  ```
- **길이**: 2분 정도 (한 곡의 후렴까지 들려야 발음·구조가 체감됨)
- **용도**: 한국어 가사 + 메타 태그의 결과 시연.

---

## 채운 후 검증

### 파일 누락 점검

```bash
# 강의 폴더 안에서 실행
cd lectures/26-04-27-ai-music

# 이미지·오디오 모두 한 번에 추출 + 누락 점검
grep -hoE "(/images|\./public/images|/audio)/[a-z0-9.-]+\.(png|jpg|jpeg|webp|mp3|wav|m4a|mp4|webm)" \
  slides.md lecture.md | sort -u | while read p; do
  rel="$(echo "$p" | sed -E 's|^\./public/|public/|; s|^/|public/|')"
  [ -f "$rel" ] || echo "MISSING: $rel  (referenced as $p)"
done
```

### 빌드 재확인

```bash
cd /home/giveroot/Projects/LocalSync/lecture
make article-html LECTURE=lectures/26-04-27-ai-music   # 경고 없는지
make slidev-html  LECTURE=lectures/26-04-27-ai-music   # dist/ 정상 빌드
make slidev-pdf   LECTURE=lectures/26-04-27-ai-music   # PDF에서 이미지 잘 들어가는지
```

### 브라우저 확인

```bash
cd lectures/26-04-27-ai-music
bun run dev
# http://localhost:3030 → 첫 슬라이드부터 끝까지 → 키로 넘기며
# image-right · cover · compare · audio 슬라이드 각각 확인
```

---

## 시간 견적

| 작업 | 예상 시간 |
|---|---|
| 다이어그램 4개 (AI 생성) | 30-40분 (프롬프트 반복 1-2회) |
| UI 스크린샷 7개 (캡처+편집) | 20-30분 |
| Remix 비교 2개 (Suno 작업) | 10-15분 |
| 오디오 3개 (Gemini + Suno) | 15-20분 (생성 시간 포함) |
| **합계** | **약 1시간 30분** |

강의 전 1주일 안에 한 번에 처리하는 것을 권장. UI는 자주 바뀌므로 너무 일찍 캡처하면 강의 시점에 어색해질 수 있음.

---

## 오디오·비디오 매핑 — 곡별 프롬프트와 슬라이드 위치

실제 채워진 음원의 생성 정보·슬라이드 매핑.

### Suno 생성 (.mp3)

| 파일 | 생성 프롬프트 | 매핑 슬라이드 |
|---|---|---|
| `apricot-hammer.mp3` | `warm piano instrumental, spring walk, gentle and bright, background music` | 5.1 Instrumental 레시피 |
| `spring-light-spreads.mp3` | `Korean K-Pop, acoustic, gentle and bright, spring walk, warm, calm vocal, slow-tempo` + 한국어 가사 4줄 | 5.2 한국어 K-Pop 발라드 |
| `saturday-stillness.mp3` | "따뜻한 어쿠스틱 기타 인트로, 햇살 가득한 주말 아침" | 5.5 인디 어쿠스틱 + 보너스 1 (Persona 원본) |
| `city-heart.mp3` | 토요일의 고요함과 같은 보컬, 다른 가사. 90년대 한국 댄스, 피아노, 빠른 템포 | 보너스 1 (Persona 변형) |
| `wet-afternoon.mp3` | `ambient dream pop ballad, meditative, slow tempo, floating synth, distant guitar, breathy vocal, melancholy but comforting` | 보너스 2 (드림 팝) + Cover 원본 |
| `wet-afternoon-x-apricot-hammer-mashup.mp3` | 두 곡 매시업 | 7-1 Cover 데모 (after) |
| `patpat-waiting.mp3` | `Kids pop lullaby, 72 BPM, soft acoustic guitar, glockenspiel, hand claps, childlike vocal` | 보너스 2 (자장가) |
| `turn-up-the-audio.mp3` | "AI 음악 생성을 공부하는 학생들" 메타 안내문 | 마지막 end 슬라이드 BGM (autoplay) |
| `3.3-gemini-spring-walk.mp3` | Gemini Fast, "잔잔한 피아노 중심의 봄 산책 배경음악" 30초 | 3.3 Gemini 결과 (audio) |

### Gemini Lyria 생성 (.mp4 = 앨범커버 + 오디오)

| 파일 | 생성 프롬프트 | 매핑 슬라이드 |
|---|---|---|
| `speed-of-light-curiosity.mp3 / .mp4` | "AI 활용을 공부하고 배우는 사람들을 위한 경쾌한 노래" | **cover BGM (autoplay loop, 우하단 컨트롤)** + 오프닝 직후 미리보기 슬라이드 (mp4) |
| `our-new-blueprint.mp3 / .mp4` | 영감·차분 (Gemini Lyria) | end 직전 보너스 비디오 슬라이드 |
| `nine-am-window-seat.mp4` | "따뜻한 어쿠스틱 기타 인트로, 햇살 가득한 주말 아침" (Gemini) | 3.3 Gemini 결과 시연 (mp4) |
| `table-by-the-window.mp4` | "카페 분위기의 로파이 힙합, 비 오는 날, 보컬 없음" (Gemini) | 3.3 Gemini 결과 시연 (mp4) |

### cover BGM 동작 메모

- `<audio autoplay loop controls>` 태그를 cover 슬라이드에 fixed-position으로 삽입.
- 브라우저 자동재생 정책: 사용자 첫 키 입력(슬라이드 넘김) 후 재생됨. 청중 입장 시점에는 무음, 첫 발표 액션과 함께 BGM 시작.
- 컨트롤은 우하단 작게 노출 → 강사가 필요 시 일시정지·볼륨 조절 가능.
- end 슬라이드의 `turn-up-the-audio.mp3`도 autoplay — 마지막 멘트 동안 자동 재생.

### lecture.md vs slides.md 분리 원칙 (재확인)

- `<audio>` `<video>` 태그는 **slides.md에만**.
- `lecture.md`에서는 텍스트 주석으로만 안내 (Pandoc `--embed-resources`가 절대경로 `/audio/...`를 root에서 찾다 실패하기 때문).

---
