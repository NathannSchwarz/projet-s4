<script setup lang="ts">
import { ref, computed } from 'vue'
import ArrowIcon2 from '@/components/icons/ArrowIcon2.vue'
import stageImage from '/public/img/Carroussel2.webp'
import alternanceImage from '/public/img/Carroussel3.webp'
import cultureImage from '/public/img/Carroussel1.webp'

interface Slide {
  image: string
  title: string
  description: string
}

const slides = ref([
  {
    image: stageImage,
    title: 'STAGE À L’ÉTRANGER',
    description: `Les stages sont une étape cruciale de la formation, et travailler au sein d'entreprises internationales leur permet de pleinement mettre en pratique le savoir appris en classe tout en découvrant un nouveau pays. Découvrez les témoignages d'étudiants et autres informations capitales ici.`,
    Bouton: 'Découvrez les stages',
  },
  {
    image: alternanceImage,
    title: 'ALTERNANCE EN EUROPE',
    description: `Très bientôt, la possibilité de faire de l'alternance dans des entreprises européennes sera envisageable ! Vous pourrez ainsi allier la théorie et la pratique en plus de vous immergez à l'international, vous permettant de pleinement découvrir comment une entreprise fonctionne.`,
    Bouton: 'Découvrez l’alternance',
  },
  {
    image: cultureImage,
    title: 'SORTIES CULTURELLES',
    description: `En plus des habituels aspects académique du BUT, MMi offre la chance aux étudiants de pouvoir partir en sortie pédagogique dans divers pays d'Europe ! Le festival OFFF à Barcelone, le Vitra Design Museum à Weil-am-Rhein, ou encore un futur semestre d'échange en Catalogne sont au programme afin d'offrir une nouvelle manière d'apprendre et de forger sa culture et sa carrière. `,
    Bouton: 'Découvrez les sorties',
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
  if (index === currentIndex.value) return 'w-10/12 md:w-8/12 xl:w-full '
  if (index === (currentIndex.value + 1) % slides.value.length)
    return 'w-1/2 md:w-1/4 xl:w-2/12 opacity-50 mx-2'
  if (index === (currentIndex.value + 2) % slides.value.length)
    return 'hidden md:flex w-1/2 md:w-1/4 xl:w-2/12 opacity-50'
  return 'hidden lg:flex w-1/3 opacity-50'
}

const handleClick = (index: number) => {
  console.log(`Clique sur l’élément : ${slides.value[index].title}`)

}

const slideOffset = computed(() => {
  return `translateX(-${currentIndex.value * 20}%)`;
});
</script>

<template>
  <div
    class="relative flex flex-col items-center justify-center  overflow-hidden mt-20 mb-44"
  >
    <!-- Carrousel -->
    <div
      class="relative w-11/12 md:w-9/12 xl:w-7/12  flex transition-transform duration-700 ease-in-out "
      :style="{ transform: slideOffset }"
    >
      <div
        v-for="(slide, index) in slides"
        :key="index"
        class="relative flex-shrink-0 transition-all duration-500 ease-in-out "
        :class="getSlideClass(index)"
      >
        <!-- Contenu principal -->
        <div class="relative h-[30rem] md:h-96 xl:h-[42rem] w-12/12 rounded-3xl overflow-hidden shadow-xl">
          <!-- Image avec Dégradé -->
          <div class="absolute inset-0">
            <img :src="slide.image" alt="Slide Image" class="h-full object-cover" />
            <div
              class="absolute inset-0 bg-gradient-to-b from-[var(--color-Rouge)] to-[var(--color-Jaune)] opacity-70"
            ></div>
          </div>

          <!-- Contenu texte pour l'élément actif -->
          <div v-if="currentIndex === index" class="absolute bottom-5 left-5 p-5">
            <h3 class="font-bold text-black">{{ slide.title }}</h3>
            <p class="mt-2 text-black text-[14px] md:text-[16px] xl:text-[18px]">{{ slide.description }}</p>
            <button
              class="text-[12px] md:text-[13px] xl:text-[14px]  mt-4 bg-[var(--color-Bleu)] px-6 py-2 rounded-xl font-semibold text-white hover:bg-[var(--color-Blanc)] hover:text-(--color-Bleu) transition-all duration-500 cursor-pointer"
              @click="handleClick(index)"
            >
              {{ slide.Bouton }}
            </button>
          </div>
        </div>

        <!-- Texte sur le côté gauche (orienté à 90°) pour l'élément actif -->
        <div
          v-if="currentIndex === index"
          class="absolute left-[-193px] top-1/2 -translate-y-1/2 text-white text-xl font-bold rotate-90 opacity-30 text-[40px] md:text-[16px] xl:text-[18px]"
        >
          {{ slide.title }}
        </div>
      </div>
    </div>

    <!-- Boutons de navigation -->
    <div class="flex gap-10 mt-5">
      <button
        class="text-black cursor-pointer rotate-180 hover:text-(--color-Rouge) transition-all duration-500"
        @click="prevSlide"
      >
        <ArrowIcon2 />
      </button>
      <button
        class="text-black cursor-pointer hover:text-(--color-Rouge) transition-all duration-500"
        @click="nextSlide"
      >
        <ArrowIcon2 />
      </button>
    </div>
  </div>
</template>
