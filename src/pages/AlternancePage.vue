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
      ALTERNANCE
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

  <section class="w-11/12 md:w-9/12 xl:w-7/12 mx-auto">
    <div class="mb-20">
      <h4 class="text-(--color-Rouge) mb-4">L’Alternance en Europe – Une opportunité en devenir</h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        L’alternance est une expérience formatrice qui permet de combiner études et immersion en
        entreprise. Aujourd’hui, les étudiants du MMi peuvent réaliser leur alternance en France,
        mais une nouvelle opportunité se dessine : l’alternance en Europe.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        L’IUT explore actuellement la possibilité de développer des partenariats avec des
        entreprises européennes afin de permettre aux étudiants de réaliser leur alternance à
        l’international, tout en poursuivant leur formation en France.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Pourquoi envisager une alternance en Europe ?
      </p>
    </div>

    <div class="mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Où en est le projet ?</h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        L’alternance à l’étranger est encore en phase de réflexion au sein du département MMi. L’IUT
        travaille actuellement à établir des contacts avec des entreprises et institutions en
        Europe, dans des secteurs comme :
      </p>
      <ul class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        <li>Le design et l’UX/UI → Studios créatifs en Allemagne, aux Pays-Bas ou en Suède.</li>
        <li>Le développement web et numérique → Startups tech à Barcelone, Berlin ou Amsterdam.</li>
        <li>La communication et le marketing digital → Agences à Madrid, Bruxelles ou Milan.</li>
      </ul>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Les enseignants du MMi encouragent déjà les étudiants à participer à des événements
        internationaux, comme le OFFF Festival de Barcelone (voir page dédié) , afin de développer
        leur réseau professionnel et de se préparer à une future expérience en entreprise à
        l’étranger.
      </p>
    </div>

    <div class="mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Comment se préparer dès maintenant ?</h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Même si le programme officiel n’est pas encore lancé, il est possible d’anticiper cette
        opportunité en :
      </p>
    </div>

    <div class="mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Restez informé sur l’évolution du projet !</h4>
    </div>
  </section>

  <section class="w-11/12 md:w-9/12 xl:w-7/12 mx-auto">
    <div class="mb-20">
      <h4 class="text-(--color-Rouge) mb-4">
        Stages à l’étranger : une inspiration pour les futurs alternants
      </h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Nos anciens étudiants ont vécu des stages en Europe, découvrant de nouvelles méthodes de
        travail, développant leurs compétences et élargissant leur réseau. Leurs expériences offrent
        un aperçu concret de ce que pourrait être l’alternance à l’international, une opportunité en
        cours de développement au MMi.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        De Berlin à Barcelone, ces témoignages montrent à quel point travailler à l’étranger est un
        atout. L’alternance en Europe suivra cette dynamique, combinant études et immersion
        professionnelle.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Découvrez leurs parcours et projetez-vous dans votre futur à l’international !
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
      class="p-5 py-7 lg:p-10 lg:py-7 bg-gradient-to-b from-[var(--color-Jaune)] to-[var(--color-Blanc)] lg:bg-gradient-to-r lg:from-[var(--color-Blanc)] lg:to-[var(--color-Jaune)] text-(--color-Blanc) grid grid-cols-1 lg:grid-cols-9 gap-5 lg:gap-6 lg:items-center lg:justify-center inset-shadow-md rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[80px] lg:rounded-tr-[20px] lg:rounded-bl-[20px] lg:rounded-br-[80px] my-20 lg:my-40"
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
