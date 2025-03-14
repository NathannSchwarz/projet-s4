<template>
  <div class="relative lg:col-span-6">
    <video ref="videoPlayer" :class="['w-full', 'shadow-xl', videoClasses]" :src="videoSrc"></video>
    <div class="absolute inset-0 flex items-center justify-center">
      <button @click="togglePlayPause" class="text-white focus:outline-none cursor-pointer">
        <svg v-if="!isPlaying" class="w-10 h-10" viewBox="0 0 24 24" fill="currentColor">
          <path d="M8 5.14v14l11-7-11-7z" />
        </svg>
        <svg v-else class="w-10 h-10" viewBox="0 0 24 24" fill="currentColor">
          <path d="M6 5.14h4v14h-4V5.14zm8 0h4v14h-4V5.14z" />
        </svg>
      </button>
      <button @click="toggleFullScreen" class="ml-4 text-white focus:outline-none cursor-pointer">
        <svg class="w-10 h-10" viewBox="0 0 24 24" fill="currentColor">
          <path d="M3 3h6v6H3zm12 0h6v6h-6zm0 12h6v6h-6zm-12 6h6v6H3zM15 15h6v6h-6z" />
        </svg>
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, watch } from 'vue'

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
