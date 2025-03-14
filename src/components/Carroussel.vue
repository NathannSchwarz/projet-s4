<template>
  <div class="relative flex items-center justify-center overflow-hidden w-full">
    <!-- Carrousel -->
    <div class="relative flex transition-all duration-500 ease-in-out w-full flex-nowrap">
      <div
        v-for="(slide, index) in slides"
        :key="index"
        class="relative flex-shrink-0 transition-all duration-500 ease-in-out"
        :class="getSlideClass(index)"
      >
        <!-- Contenu principal -->
        <div
          class="relative h-80 md:h-96 xl:h-[500px] rounded-lg overflow-hidden w-full"
          :class="{ 'shadow-xl': currentIndex === index }"
        >
          <!-- Image avec Dégradé -->
          <div class="absolute inset-0">
            <img :src="slide.image" alt="Slide Image" class="w-full h-full object-cover" />
            <div
              class="absolute inset-0 bg-gradient-to-b from-[var(--color-Rouge)] to-[var(--color-Jaune)] opacity-70"
            ></div>
          </div>

          <!-- Contenu texte pour l'élément actif -->
          <div v-if="currentIndex === index" class="absolute bottom-5 left-5 text-white">
            <h3 class="text-2xl font-bold">{{ slide.title }}</h3>
            <p class="mt-2 text-lg">{{ slide.description }}</p>
            <button
              class="mt-4 bg-[var(--color-Bleu)] px-6 py-2 rounded-lg font-semibold"
              @click="handleClick(index)"
            >
              Découvrez les stages disponibles avec l'IUT
            </button>
          </div>
        </div>

        <!-- Texte sur le côté gauche (orienté à 90°) pour l'élément actif -->
        <div
          v-if="currentIndex === index"
          class="absolute left-[-50px] top-1/2 -translate-y-1/2 text-white text-xl font-bold rotate-90"
        >
          {{ slide.title }}
        </div>
      </div>
    </div>

    <!-- Boutons de navigation -->

    <button class="text-black" @click="prevSlide">◀</button>
    <button class="text-black" @click="nextSlide">▶</button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

interface Slide {
  image: string
  title: string
  description: string
}

const slides = ref<Slide[]>([
  {
    image: 'https://via.placeholder.com/800x500',
    title: 'STAGE À L’ÉTRANGER',
    description: 'Une opportunité unique d’explorer le monde et d’apprendre.',
  },
  {
    image: 'https://via.placeholder.com/800x500',
    title: 'ALTERNANCE INTERNATIONALE',
    description: 'Combinez études et travail dans un cadre international.',
  },
  {
    image: 'https://via.placeholder.com/800x500',
    title: 'EXPÉRIENCE CULTURELLE',
    description: 'Découvrez de nouvelles cultures à travers le voyage.',
  },
])

const currentIndex = ref<number>(0)

const nextSlide = () => {
  currentIndex.value = (currentIndex.value + 1) % slides.value.length
}

const prevSlide = () => {
  currentIndex.value = (currentIndex.value - 1 + slides.value.length) % slides.value.length
}

const getSlideClass = (index: number): string => {
  if (index === currentIndex.value) return 'w-9/12 md:w-9/12 xl:w-7/12 mx-2'
  if (index === (currentIndex.value + 1) % slides.value.length)
    return 'w-1/2 md:w-1/4 xl:w-1/6 opacity-70 mx-2'
  if (index === (currentIndex.value + 2) % slides.value.length)
    return 'hidden md:flex w-1/6 opacity-50 mx-2'
  return 'hidden lg:flex w-1/6 opacity-50 mx-2'
}

const handleClick = (index: number) => {
  console.log(`Clique sur l’élément : ${slides.value[index].title}`)
}
</script>
