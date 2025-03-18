<template>
  <section ref="sectionRef" class="relative w-full overflow-hidden">
    <!-- Conteneur de la vidéo (plein écran au début, pas d'arrondi initial, overflow hidden) -->
    <div
      ref="videoContainer"
      class="w-full h-screen flex items-center justify-center z-10 overflow-hidden"
      style="position: absolute; top: 0; left: 0; border-radius: 0"
    >
      <video
        class="object-cover w-full h-full z-20"
        :src="videoSrc"
        autoplay
        loop
        muted
        playsinline
      />
    </div>

    <!-- Image derrière (z-0) -->
    <img
      class="absolute top-1/2 left-1/2 mt-6 transform -translate-x-1/2 -translate-y-1/2 xl:h-[85vh] xl:w-5/12 object-cover z-0"
      src="/img/Stars.webp"
      alt=""
    />

    <!-- Titre principal (z-2) -->
    <h1
      ref="titleRef"
      class="relative text-center text-4xl font-bold z-2 mt-32 -mb-60 text-outline"
      style="color: white"
    >
      {{ title }}
    </h1>

    <!-- Placeholder vidéo (z-10) -->
    <div ref="videoPlaceholder" class="mx-auto mt-40 w-5/12 h-[45vh] z-10 -mb-36 rounded-2xl"></div>

    <!-- Sous-titre (z-2) -->
    <h2
      ref="subtitleRef"
      class="relative text-center text-2xl mt-10 z-2 text-outline"
      style="color: white"
    >
      {{ subtitle }}
    </h2>
  </section>
</template>

<script setup lang="ts">
import { ref, onMounted, nextTick, defineProps } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

const props = defineProps({
  title: {
    type: String,
    default: 'EXPLOREZ',
  },
  subtitle: {
    type: String,
    default: "L'EUROPE",
  },
  videoSrc: {
    type: String,
    default: '/video/IUT.mp4',
  },
})

const sectionRef = ref<HTMLElement | null>(null)
const videoContainer = ref<HTMLDivElement | null>(null)
const videoPlaceholder = ref<HTMLDivElement | null>(null)
const titleRef = ref<HTMLElement | null>(null)
const subtitleRef = ref<HTMLElement | null>(null)

onMounted(async () => {
  if (
    !sectionRef.value ||
    !videoContainer.value ||
    !videoPlaceholder.value ||
    !titleRef.value ||
    !subtitleRef.value
  ) {
    return
  }

  await nextTick()

  const section = sectionRef.value
  const container = videoContainer.value
  const placeholder = videoPlaceholder.value
  const title = titleRef.value
  const subtitle = subtitleRef.value

  const mm = gsap.matchMedia()

  // À partir de 1024px
  mm.add('(min-width: 1024px)', () => {
    const tl = gsap.timeline({
      scrollTrigger: {
        trigger: section,
        start: 'top top',
        end: 'bottom top',
        pin: section,
        scrub: true,
      },
    })

    let containerRect: DOMRect
    let placeholderRect: DOMRect

    const refreshPositions = () => {
      containerRect = container.getBoundingClientRect()
      placeholderRect = placeholder.getBoundingClientRect()
    }

    refreshPositions()
    ScrollTrigger.addEventListener('refresh', refreshPositions)
    ScrollTrigger.refresh()

    // Calcule la scale
    const scaleX = () => placeholderRect.width / containerRect.width
    const scaleY = () => placeholderRect.height / containerRect.height
    const finalScale = () => Math.min(scaleX(), scaleY())

    // Décalage X / Y
    const deltaX = () =>
      placeholderRect.left +
      placeholderRect.width / 2 -
      (containerRect.left + containerRect.width / 2)

    const deltaY = () =>
      placeholderRect.top +
      placeholderRect.height / 2 -
      (containerRect.top + containerRect.height / 2)

    // Animation : la vidéo se redimensionne et arrondit le conteneur
    tl.to(container, {
      // Par exemple, un arrondi à 50% => forme circulaire
      // ou à 100px => arrondi plus léger
      borderRadius: '70px',
      scale: () => finalScale(),
      x: () => deltaX(),
      y: () => deltaY(),
      ease: 'none',
    })

    // Apparition des titres (20% du scroll)
    tl.to(
      [title, subtitle],
      {
        opacity: 1,
        duration: 0.5,
      },
      0.2,
    )
  })
})
</script>

<style scoped>
.text-outline {
  text-shadow:
    1px 1px 0 black,
    -1px -1px 0 black,
    1px -1px 0 black,
    -1px 1px 0 black;
}
</style>
