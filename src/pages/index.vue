<script setup lang="ts">
import CarteIcon from '@/components/icons/CarteIcon.vue'
import VideoPlayer from '@/components/VideoPlayer.vue'


</script>

<template>
  <section class="relative overflow-hidden py-30 xl:py-32 flex flex-col items-center mx-auto">
    <!-- Image en arrière-plan -->
    <img
      class="absolute h-[75vh] md:h-[85vh] lg:h-[70vh] xl:h-[85vh] xl:w-1/3 object-cover z-0"
      src="/img/Stars.webp"
      alt=""
    />

    <!-- Titre principal -->
    <h1 class="relative text-(--color-Blanc) text-outline z-10 text-center text-4xl xl:text-6xl">
      EXPLOREZ
    </h1>

    <!-- Conteneur de la vidéo avec hauteur fixe -->
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

    <!-- Sous-titre légèrement sous la vidéo -->
    <h2
      class="relative text-(--color-Blanc) text-outline z-10 text-center text-3xl xl:text-5xl md:-mt-6 xl:-mt-10"
    >
      L'EUROPE
    </h2>
  </section>

  <section class="relative overflow-hidden py-44 my-4 lg:my-20">
    <!-- Image de fond centrée et recadrée -->
    <div
      class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[200vw] h-[200vh] md:w-full md:h-full"
    >
      <CarteIcon class="w-full h-full object-cover" />
    </div>

    <!-- Conteneur de la grille centré verticalement -->
    <div class="flex items-center justify-center min-h-[80vh] w-11/12 md:w-9/12 xl:w-7/12 mx-auto">
      <div class="grid grid-cols-12 gap-3 lg:gap-5">
        <!-- Cartes -->
        <div
          class="bg-(--color-Blanc)/50 text-(--color-Noir) text-center drop-shadow-lg backdrop-blur-xl rounded-xl p-8 px-5 md:px-28 lg:p-10 col-span-12 lg:col-span-6 lg:rounded-3xl"
        >
          <h3>53000</h3>
          <h6>
            étudiants et personnels français en mobilité Erasmus+ sont partis étudier dans les pays
            d’Europe en 2022
          </h6>
        </div>
        <div
          class="bg-(--color-Jaune) text-(--color-Noir) text-center drop-shadow-lg rounded-xl p-8 px-3 lg:p-10 flex justify-center items-center col-span-6 lg:col-span-3 lg:rounded-3xl"
        >
          <img
            class="w-4/5 md:w-2/3 lg:w-44"
            src="/public/img/logo/logoprojet1.png"
            alt="logoiut"
          />
        </div>
        <div
          class="bg-(--color-Blanc)/50 text-(--color-Noir) text-center drop-shadow-lg backdrop-blur-xl rounded-xl p-8 px-3 md:px-10 lg:p-10 lg:px-6 col-span-6 lg:col-span-3 lg:rounded-3xl"
        >
          <h3>+ 378</h3>
          <h6>Stages à l’étranger depuis 2014 dans l’IUT NFC</h6>
        </div>
        <div
          class="bg-(--color-Rouge) text-(--color-Noir) text-center drop-shadow-lg rounded-xl p-8 px-3 md:px-10 lg:p-10 flex justify-center items-center col-span-6 lg:col-span-3 lg:rounded-3xl hidden lg:flex"
        >
          <img
            class="w-3/5 md:w-2/5 lg:w-28"
            src="/public/img/logo/logoprojet2.png"
            alt="logoiut"
          />
        </div>

        <div
          class="bg-(--color-Blanc)/50 text-(--color-Noir) text-center drop-shadow-lg backdrop-blur-xl rounded-xl p-8 px-3 lg:p-10 lg:px-6 col-span-6 lg:col-span-3 lg:rounded-3xl"
        >
          <h3>+ 378</h3>
          <h6>Stages à l’étranger depuis 2014 dans l’IUT NFC</h6>
        </div>
        <div
          class="bg-(--color-Rouge) text-(--color-Noir) text-center drop-shadow-lg rounded-xl p-8 px-3 md:px-10 lg:p-10 flex justify-center items-center col-span-6 lg:col-span-3 lg:rounded-3xl lg:hidden"
        >
          <img
            class="w-3/5 md:w-2/5 lg:w-28"
            src="/public/img/logo/logoprojet2.png"
            alt="logoiut"
          />
        </div>
        <div
          class="bg-(--color-Blanc)/50 text-(--color-Noir) text-center drop-shadow-lg backdrop-blur-xl rounded-xl p-8 px-5 md:px-28 lg:p-10 col-span-12 lg:col-span-6 lg:rounded-3xl"
        >
          <h3>53000</h3>
          <h6>
            étudiants et personnels français en mobilité Erasmus+ sont partis étudiés dans les pays
            d’Europe en 2022
          </h6>
        </div>
        <div
          class="bg-(--color-Blanc)/50 text-(--color-Noir) text-center drop-shadow-lg backdrop-blur-xl rounded-xl p-8 px-3 md:px-10 lg:p-10 lg:px-6 col-span-6 lg:col-span-3 lg:rounded-3xl"
        >
          <h3>+ 16%</h3>
          <h6>De français en mobilité à l’étranger depuis 2016</h6>
        </div>
        <div
          class="bg-(--color-Turquoise) text-(--color-Noir) text-center drop-shadow-lg rounded-xl p-8 px-3 lg:p-10 flex justify-center items-center col-span-6 lg:col-span-4 lg:hidden lg:rounded-3xl"
        >
          <img
            class="w-1/2 md:w-1/3 lg:w-24"
            src="/public/img/logo/logoprojet6.png"
            alt="logoiut"
          />
        </div>
        <div
          class="bg-(--color-Blanc)/50 text-(--color-Noir) text-center drop-shadow-lg backdrop-blur-xl rounded-xl p-8 px-5 md:px-28 lg:p-10 col-span-12 lg:col-span-6 lg:rounded-3xl"
        >
          <h3>53000</h3>
          <h6>
            étudiants et personnels français en mobilité Erasmus+ sont partis étudiés dans les pays
            d’Europe en 2022
          </h6>
        </div>
        <div
          class="bg-(--color-Turquoise) text-(--color-Noir) text-center drop-shadow-lg rounded-xl p-8 px-3 lg:p-10 flex justify-center items-center col-span-6 lg:col-span-3 hidden lg:flex lg:rounded-3xl"
        >
          <img class="w-1/2 lg:w-24" src="/public/img/logo/logoprojet6.png" alt="logoiut" />
        </div>
      </div>
    </div>
  </section>

  <section class="w-11/12 md:w-9/12 xl:w-7/12 mx-auto">
    <div class="mb-44">
      <h4 class="text-(--color-Rouge) mb-4">L'Europe : un terrain de jeu professionnel</h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Chaque année, des étudiants en MMI partent en stage, alternance et profitent des différents
        voyages organisés dans divers pays d'Europe. C'est ainsi l'occasion d'enrichir son parcours
        académique et sa culture, tout en découvrant les différents pays d'Europe ! <br /><br />
        Les expériences concrètes et enrichissantes au sein d'entreprises sont une véritable
        opportunité qui sera importante pour la carrière de nos étudiants. Le tout est encadré par
        les enseignants référents de l'Université, qui n'hésiteront pas à vous aidez concernant les
        démarches et demandes de bourses.
      </p>
    </div>

    <div class="mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Ils l’ont fait, pourquoi pas vous ?</h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Partir à l’étranger, c’est bien plus qu’une simple expérience académique : c’est une
        aventure humaine et professionnelle qui transforme une carrière. Que ce soit en stage, en
        échange universitaire ou en alternance, nos anciens étudiants ont franchi le pas et
        partagent ici leur parcours. <br /><br />
        Découvrez à travers leurs témoignages leurs défis, leurs réussites, leurs anecdotes, et
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
          Léa LEBEZIER
        </p>
        <p class="text-[13px] md:text-[14px] xl:text-[16px] font-poppins">
          "J’ai toujours voulu travailler dans un environnement international, et mon stage à Berlin
          a été une révélation !"
        </p>
        <button
          class="cursor-pointer bg-(--color-Bleu) w-full md:w-1/2 lg:w-full py-2 lg:py-3 lg:px-5 font-semibold text-[12px] md:text-[13px] xl:text-[14px] font-poppins inset-shadow-md transition-all duration-500 hover:shadow-lg hover:inset-shadow-none hover:bg-(--color-Blanc) hover:text-(--color-Bleu) rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px]"
        >
          <RouterLink to="/">Découvrez d’autres expériences !</RouterLink>
        </button>
      </div>

      <!-- Vidéo avec box shadow -->
      <VideoPlayer
        videoSrc="/video/IUT.mp4"
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
          Maxime ILUTISUQ
        </p>
        <p class="text-[13px] md:text-[14px] xl:text-[16px] font-poppins">
          "Travailler en alternance dans une agence de communication à Madrid, c’était l’opportunité
          parfaite pour allier études et expérience internationale !"
        </p>
        <button
          class="cursor-pointer bg-(--color-Bleu) w-full md:w-1/2 lg:w-full py-2 lg:py-3 lg:px-5 font-semibold text-[12px] md:text-[13px] xl:text-[14px] font-poppins inset-shadow-md transition-all duration-500 hover:shadow-lg hover:inset-shadow-none hover:bg-(--color-Blanc) hover:text-(--color-Bleu) rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px]"
        >
          <RouterLink to="/">Découvrez d’autres expériences !</RouterLink>
        </button>
      </div>

      <!-- Vidéo avec box shadow -->
      <VideoPlayer
        videoSrc="/video/IUT.mp4"
        videoClasses="rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[80px] lg:rounded-tr-[20px] lg:rounded-bl-[20px] lg:rounded-br-[80px]"
      />
    </div>

    <div
      class="p-5 py-7 lg:p-10 lg:py-7 bg-gradient-to-b from-[var(--color-Jaune)] to-[var(--color-Blanc)] lg:bg-gradient-to-r lg:from-[var(--color-Jaune)] lg:to-[var(--color-Blanc)] text-(--color-Blanc) grid grid-cols-1 lg:grid-cols-9 gap-5 lg:gap-8 lg:items-center lg:justify-center inset-shadow-md rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px] mb-20 lg:mb-40"
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
          <RouterLink to="/">Découvrez d’autres expériences !</RouterLink>
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
