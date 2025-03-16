<template>
  <div class="relative lg:col-span-6 z-40">
    <video
      ref="videoPlayer"
      :class="['w-full', 'shadow-xl', videoClasses]"
      :src="videoSrc"
      preload="auto"
      playsinline
    ></video>
    <div class="absolute inset-0 flex items-center justify-center">
      <button @click="togglePlayPause" class="text-white focus:outline-none cursor-pointer">
        <svg v-if="!isPlaying" class="w-10 h-10" viewBox="0 0 24 24" fill="currentColor">
          <path d="M8 5.14v14l11-7-11-7z" />
        </svg>
        <svg v-else class="w-10 h-10" viewBox="0 0 24 24" fill="currentColor">
          <path d="M6 5.14h4v14h-4V5.14zm8 0h4v14h-4V5.14z" />
        </svg>
      </button>
      <button
        @click="toggleFullScreen"
        class="ml-4 text-white focus:outline-none cursor-pointer hidden lg:flex"
      >
        <svg
          width="30"
          height="30"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M4 9V6C4 5.46957 4.21071 4.96086 4.58579 4.58579C4.96086 4.21071 5.46957 4 6 4H9M20 15V18C20 18.5304 19.7893 19.0391 19.4142 19.4142C19.0391 19.7893 18.5304 20 18 20H15M15 4H18C18.5304 4 19.0391 4.21071 19.4142 4.58579C19.7893 4.96086 20 5.46957 20 6V9M9 20H6C5.46957 20 4.96086 19.7893 4.58579 19.4142C4.21071 19.0391 4 18.5304 4 18V15"
            stroke="currentcolor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, watch } from 'vue'

import { onMounted } from 'vue'

onMounted(() => {
  if (videoPlayer.value) {
    videoPlayer.value.load()
  }
})

interface ExtendedHTMLVideoElement extends HTMLVideoElement {
  mozRequestFullScreen?: () => Promise<void>
  webkitRequestFullscreen?: () => Promise<void>
  msRequestFullscreen?: () => Promise<void>
}

const props = defineProps<{ videoSrc: string; videoClasses?: string }>()

const videoPlayer = ref<ExtendedHTMLVideoElement | null>(null)
const isPlaying = ref<boolean>(false)

const togglePlayPause = () => {
  if (videoPlayer.value) {
    if (videoPlayer.value.paused) {
      videoPlayer.value.play()
      isPlaying.value = true
    } else {
      videoPlayer.value.pause()
      isPlaying.value = false
    }
  }
}

const toggleFullScreen = () => {
  if (videoPlayer.value) {
    const video = videoPlayer.value
    if (video.requestFullscreen) {
      video.requestFullscreen()
    } else if (video.mozRequestFullScreen) {
      // Firefox
      video.mozRequestFullScreen()
    } else if (video.webkitRequestFullscreen) {
      // Chrome, Safari and Opera
      video.webkitRequestFullscreen()
    } else if (video.msRequestFullscreen) {
      // IE/Edge
      video.msRequestFullscreen()
    }
  }
}

// Réinitialiser l'état de lecture lorsque la source vidéo change
watch(
  () => props.videoSrc,
  () => {
    isPlaying.value = false
    if (videoPlayer.value) {
      videoPlayer.value.pause()
      videoPlayer.value.load()
    }
  },
)
</script>
