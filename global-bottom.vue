<template>
  <div class="lecture-footer">
    <span class="footer-title">AI를 활용한 나만의 음악 및 음원 작곡하기</span>
    <span class="footer-sep">·</span>
    <span>2026-04-27</span>
    <span class="footer-sep">·</span>
    <span>ExpandSource</span>
    <span class="footer-page">{{ currentPage }} / {{ total }}</span>
  </div>
</template>

<script setup lang="ts">
import { useNav } from '@slidev/client'
import { onMounted, onBeforeUnmount } from 'vue'

const { currentPage, total } = useNav()

// 한 번에 한 개의 audio/video만 재생되게 동기화.
// 다른 미디어가 play 이벤트 → 나머지 모두 pause.
// cover BGM이 있어도 사용자가 5.x 등에서 다른 곡을 누르면 자연스럽게 멈춤.
let stopOthers: ((e: Event) => void) | null = null

onMounted(() => {
  stopOthers = (e: Event) => {
    const target = e.target as HTMLMediaElement
    document.querySelectorAll<HTMLMediaElement>('audio, video').forEach((el) => {
      if (el !== target && !el.paused) {
        el.pause()
      }
    })
  }
  // capture phase: 자식 요소까지 모두 잡기
  document.addEventListener('play', stopOthers, true)
})

onBeforeUnmount(() => {
  if (stopOthers) {
    document.removeEventListener('play', stopOthers, true)
  }
})
</script>

<style scoped>
.lecture-footer {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  height: 22px;
  display: flex;
  align-items: center;
  gap: 5px;
  padding: 0 1.4em;
  font-size: 10px;
  font-family: 'Pretendard Variable', Pretendard, sans-serif;
  letter-spacing: -0.01em;
  color: rgba(100, 116, 139, 0.55);
  border-top: 1px solid rgba(100, 116, 139, 0.13);
  pointer-events: none;
  z-index: 200;
}

.footer-sep {
  opacity: 0.4;
}

.footer-page {
  margin-left: auto;
}
</style>
