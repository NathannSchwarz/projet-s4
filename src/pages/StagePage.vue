<script setup lang="ts">
import VideoPlayer from '@/components/VideoPlayer.vue'
import VideoIntro from '@/components/VideoAccueil.vue'

const scrollToTop = () => {
  window.scrollTo(0, 0);
}

import { ref } from 'vue'

const showText = ref(false)

const showText1 = ref(false)
const showText2 = ref(false)
const showText3 = ref(false)

const toggleText = () => {
  showText.value = !showText.value
}
const toggleText1 = () => {
  showText1.value = !showText1.value
}
const toggleText2 = () => {
  showText2.value = !showText2.value
}
const toggleText3 = () => {
  showText3.value = !showText3.value
}
</script>

<template>
  <VideoIntro
    title="STAGE"
    subtitle="EN EUROPE"
    videoSrc="/video/IUT.mp4"
    class="hidden xl:block"
  />
  <section
    class="block xl:hidden relative overflow-hidden py-30 xl:py-28 flex flex-col items-center mx-auto"
  >
    <!-- Image en arrière-plan -->
    <img
      class="absolute h-[75vh] md:h-[85vh] lg:h-[70vh] xl:h-[85vh] xl:w-1/3 object-cover z-0"
      src="/img/Stars.webp"
      alt=""
    />

    <!-- Titre principal -->
    <h1 class="relative text-(--color-Blanc) text-outline z-10 text-center text-4xl xl:text-6xl">
      STAGE
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
      EN EUROPE
    </h2>
  </section>

  <img
    src="/public/img/CarteStage.webp"
    alt="Carte Stage"
    class="h-[40rem] object-cover overflow-hidden mb-20 lg:my-44 lg:mb-60 mx-auto lg:w-9/12 xl:w-7/12 lg:h-auto"
  />

  <div class="w-11/12 md:w-9/12 xl:w-7/12 mx-auto">
    <div class="mb-20 space-y-4">
      <h4 class="text-(--color-Rouge) mb-4">Faire un stage à l'étranger</h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Chaque année , des étudiants effectuent
        <span class="font-semibold"
          >un stage à l’étranger, en Europe ou sur d’autres continents</span
        >. La proximité avec la Suisse romande et alémanique est particulièrement attractive pour
        les étudiants. Effectuer un ou plusieurs stages à l’étranger permet  :  
      </p>
      <ul class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins font-light">
        <li>
          • de maîtriser une langue étrangère pour améliorer son employabilité ou en vue d’une
          poursuite d’études,
        </li>
        <li>• de découvrir une autre culture,</li>
        <li>• d’approfondir ses connaissances,</li>
        <li>• de s’ouvrir un plus grand nombre de portes en sortant de l’Université,</li>
        <li>• d’avoir une expérience professionnelle et culturelle unique.</li>
      </ul>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Cette expérience constitue <span class="font-semibold">un atout supplémentaire pour l’insertion professionnelle</span>  ou  <span class="font-semibold">la
        poursuite d’études des diplômés</span> qui ont fait preuve d’autonomie, d’adaptabilité, de
        curiosité, d’ouverture d’esprit et d’audace !  Un enseignant référent par département
        accompagne les étudiants qui le souhaitent dans <span class="font-semibold">leur recherche et dans leurs démarches pour
        les demandes de bourses de mobilité</span> . 
      </p>
      <p
        class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins !font-semibold text-(--color-Rouge)"
      >
        <a
          href="https://www.google.com/maps/d/u/0/viewer?ll=37.29968222369501%2C43.38691009809611&z=2&mid=1lIgYQZtOdcm15plENMfIdcnb_Lym-GM" target="_blank"
          >> Exemples de destinations</a
        >
      </p>
    </div>
  </div>

  <section class="w-11/12 md:w-9/12 xl:w-7/12 mx-auto">
    <div class="grid grid-cols-1 md:grid-cols-12 md:grid-row-5 mb-44 lg:mb-54 gap-5">
      <div class="relative w-full group col-span-12 md:col-span-7">
        <!-- Image -->
        <img
          class="rounded-xl lg:rounded-2xl object-cover h-[90vw] w-full md:h-auto"
          src="/public/img/ville/Ville1.webp"
          alt=""
        />

        <!-- Bouton (visible en mobile) -->
        <button
          @click="toggleText"
          class="absolute top-3 left-3 bg-black/50 text-white p-1.5 rounded-full xl:hidden z-10 transition-transform duration-300"
          :class="{ 'rotate-180': showText }"
        >
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M5 7l5 5 5-5H5z" clip-rule="evenodd" />
          </svg>
        </button>

        <!-- Texte (visible au hover en desktop et au clic en mobile) -->
        <div
          class="absolute top-0 left-0 w-full h-full bg-black/60 text-white flex flex-col p-5 rounded-xl lg:rounded-2xl transition-opacity duration-500 opacity-0 lg:group-hover:opacity-100 justify-end pb-10 md:h-[28.5vw] lg:h-[28.6vw] xl:h-[22.2vw]"
          :class="{ 'opacity-100': showText }"
        >
          <h4 class="text-xl font-semibold">Lisbonne</h4>
          <p class="text-[14px] md:text-[12px] xl:text-[16px] font-poppins mt-2">
            Capitale du Portugal, c’est une ville dynamique et ensoleillée, réputée pour son mélange
            unique de tradition et de modernité. Entre ses ruelles pavées colorées, ses célèbres
            tramways jaunes et ses quartiers historiques comme l’Alfama et le Bairro Alto, elle
            offre une atmosphère chaleureuse et inspirante.
          </p>
        </div>
      </div>
      <div class="relative w-full group col-span-12 md:col-span-5 md:row-span-2">
        <!-- Image -->
        <img
          class="rounded-xl lg:rounded-2xl object-cover h-[90vw] w-full md:h-[45vw] xl:h-[32vw]"
          src="/public/img/ville/Ville4.webp"
          alt=""
        />

        <!-- Bouton (visible en mobile) -->
        <button
          @click="toggleText1"
          class="absolute top-3 left-3 bg-black/50 text-white p-1.5 rounded-full xl:hidden z-10 transition-transform duration-300"
          :class="{ 'rotate-180': showText1 }"
        >
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M5 7l5 5 5-5H5z" clip-rule="evenodd" />
          </svg>
        </button>

        <!-- Texte (visible au hover en desktop et au clic en mobile) -->
        <div
          class="absolute top-0 left-0 w-full h-full bg-black/60 text-white flex flex-col p-5 rounded-xl lg:rounded-2xl transition-opacity duration-500 opacity-0 lg:group-hover:opacity-100 justify-end pb-10 md:h-[45vw] xl:h-[32vw]"
          :class="{ 'opacity-100': showText1 }"
        >
          <h4 class="text-xl font-semibold">Madrid</h4>
          <p class="text-[14px] md:text-[12px] xl:text-[16px] font-poppins mt-2">
            Capitale de l’Espagne, Madrid est une ville effervescente et chaleureuse, réputée pour
            son ambiance festive et sa richesse culturelle. Entre ses grandes places comme la Puerta
            del Sol, son majestueux Palais Royal et ses quartiers vivants comme Malasaña et La
            Latina, elle conjugue tradition et modernité avec éclat.
          </p>
        </div>
      </div>

      <div
        class="md:hidden col-span-12 bg-(--color-Jaune) text-(--color-Noir) text-center drop-shadow-lg rounded-xl p-8 px-3 lg:p-10 flex justify-center items-center lg:rounded-3xl"
      >
        <img class="w-4/5 md:w-2/3 lg:w-44" src="/public/img/logo/logoprojet1.png" alt="logoiut" />
      </div>

      <div
        class="relative w-full group col-span-12 md:col-span-5 md:row-span-2 md:-mt-[0.5vw] xl:-mt-[0vw]"
      >
        <!-- Image -->
        <img
          class="rounded-xl lg:rounded-2xl object-cover h-[90vw] w-full md:h-[45vw] xl:h-[32vw]"
          src="/public/img/ville/Ville3.webp"
          alt=""
        />

        <!-- Bouton (visible en mobile) -->
        <button
          @click="toggleText2"
          class="absolute top-3 left-3 bg-black/50 text-white p-1.5 rounded-full xl:hidden z-10 transition-transform duration-300"
          :class="{ 'rotate-180': showText2 }"
        >
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M5 7l5 5 5-5H5z" clip-rule="evenodd" />
          </svg>
        </button>

        <!-- Texte (visible au hover en desktop et au clic en mobile) -->
        <div
          class="absolute top-0 left-0 w-full h-full bg-black/60 text-white flex flex-col p-5 rounded-xl lg:rounded-2xl transition-opacity duration-500 opacity-0 lg:group-hover:opacity-100 justify-end pb-10 md:h-[45vw] xl:h-[32vw]"
          :class="{ 'opacity-100': showText2 }"
        >
          <h4 class="text-xl font-semibold">Budapest</h4>
          <p class="text-[14px] md:text-[12px] xl:text-[16px] font-poppins mt-2">
            Capitale de la Hongrie, Budapest est une ville majestueuse et envoûtante, traversée par
            le Danube et marquée par son architecture grandiose. Entre ses bains thermaux, son
            Parlement néogothique et ses quartiers vibrants comme Buda et Pest, elle allie histoire,
            détente et dynamisme avec élégance.
          </p>
        </div>
      </div>
      <div
        class="col-span-2 md:row-span-1 hidden md:flex md:-mt-[0.5vw] md:h-[14vw] xl:-mt-[0.15vw] xl:h-[9vw] bg-(--color-Jaune) text-(--color-Noir) text-center drop-shadow-lg rounded-xl p-8 px-3 flex justify-center items-center lg:rounded-3xl"
      >
        <img class="w-4/5 md:w-12/12" src="/public/img/logo/logoprojet1.png " alt="logoiut" />
      </div>

      <div class="relative w-full col-span-12 group md:col-span-7">
        <!-- Image -->
        <img
          class="rounded-xl lg:rounded-2xl object-cover h-[90vw] w-full md:h-auto"
          src="/public/img/ville/Ville2.webp"
          alt=""
        />

        <!-- Bouton (visible en mobile) -->
        <button
          @click="toggleText3"
          class="absolute top-3 left-3 bg-black/50 text-white p-1.5 rounded-full xl:hidden z-10 transition-transform duration-300"
          :class="{ 'rotate-180': showText3 }"
        >
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M5 7l5 5 5-5H5z" clip-rule="evenodd" />
          </svg>
        </button>

        <!-- Texte (visible au hover en desktop et au clic en mobile) -->
        <div
          class="absolute top-0 left-0 w-full h-full bg-black/60 text-white flex flex-col p-5 rounded-xl lg:rounded-2xl transition-opacity duration-500 opacity-0 lg:group-hover:opacity-100 justify-end pb-10 md:h-[28.5vw] xl:h-[22.2vw]"
          :class="{ 'opacity-100': showText3 }"
        >
          <h4 class="text-xl font-semibold">Bruxelles</h4>
          <p class="text-[14px] md:text-[12px] xl:text-[16px] font-poppins mt-2">
            Capitale de la Belgique, Bruxelles est une ville cosmopolite et vibrante, connue pour
            son riche patrimoine et son esprit européen. Entre ses façades Art nouveau, sa
            Grand-Place classée à l’UNESCO et ses quartiers animés comme le Sablon et Saint-Gilles,
            elle mêle histoire et modernité avec élégance.
          </p>
        </div>
      </div>
    </div>

    <div class="mb-40 lg:mb-60 space-y-8">
      <h4 class="text-(--color-Rouge) mb-4">
        Aide à la mobilité internationale dans le cadre d'un stage
      </h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Il existe plusieurs bourses de stage à l’international, qui sont cumulables (certaines sont
        soumises à conditions de ressources).
      </p>
      <div class="space-y-4">
        <p
          class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins !font-semibold text-(--color-Rouge)"
        >
          • Bourse de stage Erasmus+
        </p>
        <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
          Candidature, informations sur les pays éligibles et conditions d’éligibilité depuis ce
          lien :  >Bourses de stage Erasmus
        </p>
        <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
          Certains étudiants peuvent bénéficier d’un complément inclusion Erasmus+, informations sur
          le montant et les conditions d’éligibilité depuis ce lien : >Complément inclusion Erasmus+
        </p>
      </div>
      <div class="space-y-4">
        <p
          class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins !font-semibold text-(--color-Rouge)"
        >
          • Dynastage
        </p>
        <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
          La Région Bourgogne Franche-Comté attribue des bourses sous conditions de ressources, les
          étudiants peuvent faire une simulation et s’informer sur les conditions d’éligibilité
          depuis le site mobilité internationale pour savoir s’ils peuvent bénéficier de cette
          bourse.
        </p>
        <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
          Pour faire une demande de bourse Dynastage, les étudiants doivent demander à leur
          secrétariat de Département un formulaire de demande de codes d’accès puis faire les
          démarches en ligne sur le lien qui leur sera communiqué lorsqu’ils auront transmis le
          formulaire complété à leur secrétariat.
        </p>
      </div>
      <div class="space-y-4">
        <p
          class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins !font-semibold text-(--color-Rouge)"
        >
          • Aide à la mobilité internationale pour les stages
        </p>
        <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
          Les étudiants bénéficiaires d’une bourse d’enseignement supérieur sur critères sociaux au
          titre de l’année universitaire en cours, ou bénéficiaires d’une allocation annuelle
          accordée dans le cadre du dispositif des aides spécifiques sont éligibles à cette bourse. 
        </p>
        <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
          Candidature, conditions d’éligibilité et informations depuis ce lien : aides pour
          financer.
        </p>
        <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
          Elle est cumulable avec la bourse d’enseignement supérieur, attribution sur critères
          sociaux (dont la demande est à effectuer du 15 janvier au 15 avril sur crous besançon)
        </p>
      </div>

      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        <a href="https://www.univ-fcomte.fr/partir-letranger#.YBlCiRbjKUk" target="_blank"
          >Cette liste n’est pas exhaustive >
          <span
            class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins !font-semibold text-(--color-Rouge)"
          >
            + d’infos
          </span></a
        >
      </p>
    </div>

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
        <h4 class="lg:mb-5">Stage en UX/UI design à Berlin</h4>
        <p class="text-[16px] md:text-[18px] xl:text-[20px] font-poppins !font-semibold">
          Gaëlle GUILLOU
        </p>
        <p class="text-[13px] md:text-[14px] xl:text-[16px] font-poppins">
          "J’ai toujours voulu travailler dans un environnement international, et mon stage à Berlin
          a été une révélation !"
        </p>

      </div>

      <!-- Vidéo avec box shadow -->
      <VideoPlayer
        videoSrc="/video/loic.mp4"
        videoClasses="rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px]"
      />
    </div>

    <div
      class="p-5 py-7 lg:p-10 lg:py-7 bg-gradient-to-b from-[var(--color-Turquoise)] to-[var(--color-Blanc)] lg:bg-gradient-to-r lg:from-[var(--color-Blanc)] lg:to-[var(--color-Turquoise)] text-(--color-Blanc) grid grid-cols-1 lg:grid-cols-9 gap-5 lg:gap-6 lg:items-center lg:justify-center inset-shadow-md rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[80px] lg:rounded-tr-[20px] lg:rounded-bl-[20px] lg:rounded-br-[80px] my-20 lg:my-40"
    >
      <!-- Conteneur des textes -->
      <div class="space-y-3 lg:col-span-3 lg:order-2">
        <h4 class="lg:mb-5">Stage en webdesign à Madrid</h4>
        <p class="text-[16px] md:text-[18px] xl:text-[20px] font-poppins !font-semibold">
          Loïc MATTERN
        </p>
        <p class="text-[13px] md:text-[14px] xl:text-[16px] font-poppins">
          "Travailler en alternance dans une agence de communication à Madrid, c’était l’opportunité
          parfaite pour allier études et expérience internationale !"
        </p>

      </div>

      <!-- Vidéo avec box shadow -->
      <VideoPlayer
        videoSrc="/video/Melissa.mp4"
        videoClasses="rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[80px] lg:rounded-tr-[20px] lg:rounded-bl-[20px] lg:rounded-br-[80px]"
      />
    </div>

    <div
      class="p-5 py-7 lg:p-10 lg:py-7 bg-gradient-to-b from-[var(--color-Jaune)] to-[var(--color-Blanc)] lg:bg-gradient-to-r lg:from-[var(--color-Jaune)] lg:to-[var(--color-Blanc)] text-(--color-Blanc) grid grid-cols-1 lg:grid-cols-9 gap-5 lg:gap-8 lg:items-center lg:justify-center inset-shadow-md rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px] mb-40 lg:mb-70"
    >
      <!-- Conteneur des textes -->
      <div class="space-y-3 lg:col-span-3">
        <h4 class="lg:mb-5">Stage en webdesign à Madrid</h4>
        <p class="text-[16px] md:text-[18px] xl:text-[20px] font-poppins !font-semibold">
          Gaëlle GUILLOU
        </p>
        <p class="text-[13px] md:text-[14px] xl:text-[16px] font-poppins">
          "Voir comment des professionnels construisent des expériences visuelles innovantes m’a
          donné une vraie motivation pour mes propres projets."
        </p>

      </div>

      <!-- Vidéo avec box shadow -->
      <VideoPlayer
        videoSrc="/video/loic.mp4"
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
