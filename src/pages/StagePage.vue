<script setup lang="ts">
import VideoPlayer from '@/components/VideoPlayer.vue'

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' })
}
</script>

<template>
  <section class="relative overflow-hidden py-30 xl:py-28 flex flex-col items-center mx-auto">
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

  <img src="/public/img/CarteStage.webp" alt="" />

  <div class="w-11/12 md:w-9/12 xl:w-7/12 mx-auto">
    <div class="mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Faire un stage à l'étranger</h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Chaque année , des étudiants effectuent un stage à l’étranger, en Europe ou sur d’autres
        continents. La proximité avec la Suisse romande et alémanique est particulièrement
        attractive pour les étudiants. Effectuer un ou plusieurs stages à l’étranger permet  : • de
        maîtriser une langue étrangère pour améliorer son employabilité ou en vue d’une poursuite
        d’études,  • de découvrir une autre culture, • d’approfondir ses connaissances, • de
        s’ouvrir un plus grand nombre de portes en sortant de l’Université, • d’avoir une expérience
        professionnelle et culturelle unique. Cette expérience constitue un atout
        supplémentaire pour l’insertion professionnelle ou la poursuite d’études des diplômés qui
        ont fait preuve d’autonomie, d’adaptabilité, de curiosité, d’ouverture d’esprit et d’audace
        !  Un enseignant référent par département accompagne les étudiants qui le souhaitent dans
        leur recherche et dans leurs démarches pour les demandes de bourses de mobilité.  > Exemples
        de destinations
      </p>
    </div>
  </div>

  <section>
    <img src="/public/img//ville/Ville1.webp" alt="" />
    <img src="/public/img//ville/Ville4.webp" alt="" />
    <div
      class="bg-(--color-Jaune) text-(--color-Noir) text-center drop-shadow-lg rounded-xl p-8 px-3 lg:p-10 flex justify-center items-center lg:rounded-3xl"
    >
      <img class="w-4/5 md:w-2/3 lg:w-44" src="/public/img/logo/logoprojet1.png" alt="logoiut" />
    </div>
    <img src="/public/img//ville/Ville3.webp" alt="" />
    <img src="/public/img//ville/Ville2.webp" alt="" />
  </section>

  <section class="w-11/12 md:w-9/12 xl:w-7/12 mx-auto">
    <div class="mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Aide à la mobilité internationale dans le cadre d'un stage</h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Il existe plusieurs bourses de stage à l’international, qui sont cumulables (certaines sont
        soumises à conditions de ressources).
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        • Bourse de stage Erasmus+
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Candidature, informations sur les pays éligibles et conditions d’éligibilité depuis ce lien
        :  >Bourses de stage Erasmus
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Certains étudiants peuvent bénéficier d’un complément inclusion Erasmus+, informations sur
        le montant et les conditions d’éligibilité depuis ce lien : >Complément inclusion Erasmus+
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">• Dynastage</p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        La Région Bourgogne Franche-Comté attribue des bourses sous conditions de ressources, les
        étudiants peuvent faire une simulation et s’informer sur les conditions d’éligibilité depuis
        le site mobilité internationale pour savoir s’ils peuvent bénéficier de cette bourse.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Pour faire une demande de bourse Dynastage, les étudiants doivent demander à leur
        secrétariat de Département un formulaire de demande de codes d’accès puis faire les
        démarches en ligne sur le lien qui leur sera communiqué lorsqu’ils auront transmis le
        formulaire complété à leur secrétariat.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        • Aide à la mobilité internationale pour les stages
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Les étudiants bénéficiaires d’une bourse d’enseignement supérieur sur critères sociaux au
        titre de l’année universitaire en cours, ou bénéficiaires d’une allocation annuelle accordée
        dans le cadre du dispositif des aides spécifiques sont éligibles à cette bourse. 
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Candidature, conditions d’éligibilité et informations depuis ce lien : aides pour financer.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Elle est cumulable avec la bourse d’enseignement supérieur, attribution sur critères sociaux
        (dont la demande est à effectuer du 15 janvier au 15 avril sur crous besançon)
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Cette liste n’est pas exhaustive > + d’infos
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
          <RouterLink to="/stage-europe" @click="scrollToTop"
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
          <RouterLink to="/stage-europe" @click="scrollToTop"
            >Découvrez d’autres expériences !</RouterLink
          >
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
          <RouterLink to="/sorties-culturelles" @click="scrollToTop"
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
