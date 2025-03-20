<script setup lang="ts">
import VideoPlayer from '@/components/VideoPlayer.vue'
import Carroussel from '@/components/CarrousselPage.vue'
import DataIntro from '@/components/DataIntro.vue'
import VideoIntro from '@/components/VideoAccueil.vue'

const scrollToTop = () => {
  window.scrollTo(0, 0);
}
</script>

<template>
  <!--
    1) Le composant « vidéo intro »
       - Masqué pour les tailles < xl
       - Visible à partir de xl
  -->

  <VideoIntro class="hidden xl:block" />

  <!--
    2) La section « fallback »
       - Visible pour les tailles < xl
       - Masqué à partir de xl
  -->
  <section
    class="block xl:hidden relative overflow-hidden py-30 xl:py-28 flex flex-col items-center mx-auto"
  >
    <img
      class="absolute h-[75vh] md:h-[85vh] lg:h-[70vh] xl:h-[85vh] xl:w-1/3 object-cover z-0"
      src="/img/Stars.webp"
      alt=""
    />
    <h1 class="relative text-(--color-Blanc) text-outline z-10 text-center text-4xl xl:text-6xl">
      EXPLOREZ
    </h1>
    <div
      class="relative h-[60vh] overflow-hidden z-20 w-11/12 md:w-9/12 lg:w-5/12 md:-mt-6 xl:-mt-14 lg:h-[45vh] nonevideo"
    >
      <video
        class="absolute top-0 left-1/2 -translate-x-1/2 w-full h-full object-cover rounded-xl xl:rounded-3xl nonevideo no-controls"
        src="/video/IUT.mp4"
        autoplay
        loop
        muted
        playsinline
      ></video>
    </div>
    <h2
      class="relative text-(--color-Blanc) text-outline z-10 text-center text-3xl xl:text-5xl md:-mt-6 xl:-mt-10"
    >
      L'EUROPE
    </h2>
  </section>

  <DataIntro />

  <div class="w-11/12 md:w-9/12 xl:w-7/12 mt-20 mx-auto lg:mt-44">
    <h4 class="text-(--color-Rouge) mb-4">L'Europe : un terrain de jeu professionnel</h4>
    <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
      Chaque année, des étudiants en MMI partent en <span class="font-semibold">stage</span> ,<span class="font-semibold">alternance</span> et profitent des différents
      voyages organisés dans <span class="font-semibold">divers pays d'Europe</span>. C'est ainsi l'occasion d'enrichir son parcours
      académique et sa culture, tout en découvrant les différents pays d'Europe ! <br /><br />
      Les expériences concrètes et enrichissantes au sein d'entreprises sont <span class="font-semibold">une véritable
      opportunité </span>qui sera importante pour la carrière de nos étudiants. Le tout est encadré par les
      enseignants référents de l'Université, qui n'hésiteront pas à vous aidez concernant les
      démarches et demandes de bourses.
    </p>
  </div>

  <Carroussel />

  <section class="w-11/12 md:w-9/12 xl:w-7/12 mx-auto">
    <div class="mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Ils l’ont fait, pourquoi pas vous ?</h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Partir à l’étranger, c’est bien plus qu’une simple expérience académique : <span class="font-semibold">c’est une
        aventure humaine et professionnelle</span>  qui transforme une carrière. Que ce soit en stage, en
        échange universitaire ou en alternance, nos anciens étudiants ont franchi le pas et
        partagent ici leur parcours. <br /><br />
        <span class="font-semibold">Découvrez à travers leurs témoignages</span> leurs défis, leurs réussites, leurs anecdotes, et
        surtout, l’impact qu’a eu cette expérience sur leur avenir. De Berlin à Madrid, en passant
        par Amsterdam et Barcelone, chaque destination offre son lot de découvertes et
        d’opportunités.
      </p>
    </div>

    <div
      class="p-5 py-7 lg:p-10 lg:py-7 bg-gradient-to-b from-[var(--color-Rouge)] to-[var(--color-Blanc)] lg:bg-gradient-to-r lg:from-[var(--color-Rouge)] lg:to-[var(--color-Blanc)] text-(--color-Blanc) grid grid-cols-1 lg:grid-cols-9 gap-5 lg:gap-8 lg:items-center lg:justify-center inset-shadow-md rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px] mb-20 lg:mb-40"
    >
      <!-- Conteneur des textes -->
      <div class="space-y-3 lg:col-span-3">
        <h4 class="lg:mb-8">Stage en UX/UI design à Berlin</h4>
        <p class="text-[16px] md:text-[18px] xl:text-[20px] font-poppins !font-semibold">
          Gaëlle GUILLOU
        </p>
        <p class="text-[13px] md:text-[14px] xl:text-[16px] font-poppins">
          "J’ai toujours voulu travailler dans un environnement international, et mon stage à Berlin
          a été une révélation !"
        </p>
        <button
          class="cursor-pointer bg-(--color-Bleu) w-full md:w-1/2 lg:w-full py-2 lg:py-3 lg:px-5 font-semibold text-[12px] md:text-[13px] xl:text-[14px] font-poppins inset-shadow-md transition-all duration-500 hover:shadow-lg hover:inset-shadow-none hover:bg-(--color-Blanc) hover:text-(--color-Bleu) rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px]"
        >
          <RouterLink to="/StagePage" @click="scrollToTop"
            >Découvrez d’autres expériences !</RouterLink
          >
        </button>
      </div>

      <!-- Vidéo avec box shadow -->
      <VideoPlayer
        videoSrc="/video/Melissa.mp4"
        videoClasses="rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px]"
      />
    </div>

    <div
      class="p-5 py-7 lg:p-10 lg:py-7 bg-gradient-to-b from-[var(--color-Turquoise)] to-[var(--color-Blanc)] lg:bg-gradient-to-r lg:from-[var(--color-Blanc)] lg:to-[var(--color-Turquoise)] text-(--color-Blanc) grid grid-cols-1 lg:grid-cols-9 gap-5 lg:gap-6 lg:items-center lg:justify-center inset-shadow-md rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[80px] lg:rounded-tr-[20px] lg:rounded-bl-[20px] lg:rounded-br-[80px] my-20 lg:my-40"
    >
      <!-- Conteneur des textes -->
      <div class="space-y-3 lg:col-span-3 lg:order-2">
        <h4 class="lg:mb-8">Stage en webdesign à Madrid</h4>
        <p class="text-[16px] md:text-[18px] xl:text-[20px] font-poppins !font-semibold">
         Loïc MATTERN
        </p>
        <p class="text-[13px] md:text-[14px] xl:text-[16px] font-poppins">
          "Travailler en alternance dans une agence de communication à Madrid, c’était l’opportunité
          parfaite pour allier études et expérience internationale !"
        </p>
        <button
          class="cursor-pointer bg-(--color-Bleu) w-full md:w-1/2 lg:w-full py-2 lg:py-3 lg:px-5 font-semibold text-[12px] md:text-[13px] xl:text-[14px] font-poppins inset-shadow-md transition-all duration-500 hover:shadow-lg hover:inset-shadow-none hover:bg-(--color-Blanc) hover:text-(--color-Bleu) rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px]"
        >
          <RouterLink to="/StagePage" @click="scrollToTop"
            >Découvrez d’autres expériences !</RouterLink
          >
        </button>
      </div>

      <!-- Vidéo avec box shadow -->
      <VideoPlayer
        videoSrc="/video/loic.mp4"
        videoClasses="rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[80px] lg:rounded-tr-[20px] lg:rounded-bl-[20px] lg:rounded-br-[80px]"
      />
    </div>

    <div
      class="p-5 py-7 lg:p-10 lg:py-7 bg-gradient-to-b from-[var(--color-Jaune)] to-[var(--color-Blanc)] lg:bg-gradient-to-r lg:from-[var(--color-Jaune)] lg:to-[var(--color-Blanc)] text-(--color-Blanc) grid grid-cols-1 lg:grid-cols-9 gap-5 lg:gap-8 lg:items-center lg:justify-center inset-shadow-md rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px] mb-40 lg:mb-70"
    >
      <!-- Conteneur des textes -->
      <div class="space-y-3 lg:col-span-3">
        <h4 class="lg:mb-8">Voyage au OFFF de Barcelone</h4>
        <p class="text-[16px] md:text-[18px] xl:text-[20px] font-poppins !font-semibold">
          Chloé VISIRE
        </p>
        <p class="text-[13px] md:text-[14px] xl:text-[16px] font-poppins">
          "Voir comment des professionnels construisent des expériences visuelles innovantes m’a
          donné une vraie motivation pour mes propres projets."
        </p>
        <button
          class="cursor-pointer bg-(--color-Bleu) w-full md:w-1/2 lg:w-full py-2 lg:py-3 lg:px-5 font-semibold text-[12px] md:text-[13px] xl:text-[14px] font-poppins inset-shadow-md transition-all duration-500 hover:shadow-lg hover:inset-shadow-none hover:bg-(--color-Blanc) hover:text-(--color-Bleu) rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px]"
        >
          <RouterLink to="/SortiesPage" @click="scrollToTop"
            >Découvrez d’autres expériences !</RouterLink
          >
        </button>
      </div>

      <!-- Vidéo avec box shadow -->
      <VideoPlayer
        videoSrc="/video/IUT.mp4"
        videoClasses="rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px]"
      />
    </div>
  </section>
</template>

<style>
.text-outline {
  text-shadow:
    1px 1px 0 black,
    -1px -1px 0 black,
    1px -1px 0 black,
    -1px 1px 0 black;
}

.nonevideo {
  pointer-events: none;
  user-select: none;
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
}
</style>
