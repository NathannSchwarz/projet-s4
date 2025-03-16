<script setup lang="ts">
import VideoPlayer from '@/components/VideoPlayer.vue'
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
      SORTIES
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
      CULTURELLES
    </h2>
  </section>

  <section class="w-11/12 md:w-9/12 xl:w-7/12 mx-auto">
    <div class="grid grid-cols-12 gap-2 lg:gap-5 py-10 mb-16 lg:py-44 lg:-mb-10">
      <img
        class="col-span-6 rounded-xl lg:rounded-2xl"
        src="/public/img/off/Off7.webp"
        alt="Off7"
      />
      <img
        class="col-span-6 mt-20 rounded-xl lg:rounded-2xl"
        src="/public/img/Vitra/Vitra5.webp"
        alt="Vitra5"
      />
      <img
        class="col-span-6 -mt-[33vw] md:-mt-[26vw] lg:-mt-[27vw] xl:-mt-[21vw] rounded-xl lg:rounded-2xl"
        src="/public/img/Vitra/Vitra6.webp"
        alt="Vitra6"
      />
      <img
        class="col-span-12 rounded-xl lg:rounded-2xl"
        src="/public/img/off/Off6.webp"
        alt="Off6"
      />
    </div>

    <div class="w-11/12 lg:w-10/12 mx-auto border-1 rounded-2xl mb-24 lg:mb-32"></div>

    <div class="mb-12 lg:mb-20">
      <h4 class="text-(--color-Rouge) mb-4">
        OFFF Festival – Plongez au cœur de la création numérique à Barcelone
      </h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Un événement incontournable pour les passionnés de design et d’innovation
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Fondé à Barcelone en 2001, OFFF est le plus grand rassemblement de la créativité
        contemporaine, où les meilleurs talents du monde entier se retrouvent pour partager leur
        processus de création et explorer l’avenir de l’industrie créative mondiale.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        OFFF est un espace dédié à l’innovation, la collaboration et l’inspiration, mêlant icônes
        établies et nouvelles voix émergentes dans les domaines de l’art, du design et de la culture
        numérique.
      </p>
      <ul class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Pendant plusieurs jours, le festival propose :
        <li>
          Des conférences inspirantes animées par des figures majeures du design et de la
          communication visuelle.
        </li>
        <li>
          Des ateliers pratiques et masterclasses pour expérimenter de nouvelles approches
          créatives.
        </li>
        <li>
          Des installations et expositions immersives mettant en avant les nouvelles tendances du
          digital.
        </li>
        <li>Un marché du design où découvrir les œuvres et productions des artistes présents.</li>
      </ul>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Les enseignants du MMi encouragent déjà les étudiants à participer à des événements
        internationaux, comme le OFFF Festival de Barcelone (voir page dédié) , afin de développer
        leur réseau professionnel et de se préparer à une future expérience en entreprise à
        l’étranger.
      </p>
    </div>

    <VideoPlayer
      videoSrc="/video/Off.mp4"
      videoClasses="rounded-xl lg:rounded-2xl mb-12 lg:mb-20"
    />

    <div class="mb-12 lg:mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Qui peut y participer ?</h4>
      <ul class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        <li>1ère année : Accessible aux meilleurs étudiants du classement.</li>
        <li>2ème & 3ème année : Ouvert aux alternants, sur proposition des enseignants.</li>
      </ul>
    </div>
    <div class="mb-12 lg:mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Pourquoi y aller ?</h4>
      <ul class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        <li>
          Assister à des conférences inspirantes de designers, directeurs artistiques et studios
          renommés.
        </li>
        <li>Découvrir les dernières tendances du design interactif et du branding digital.</li>
        <li>Rencontrer des professionnels et élargir son réseau pour son avenir.</li>
      </ul>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Un véritable tremplin pour booster sa créativité et son inspiration !
      </p>
    </div>

    <div class="grid grid-cols-12 gap-2 lg:gap-5 mb-24 lg:mb-32">
      <img
        class="rounded-xl lg:rounded-2xl col-span-6"
        src="/public/img/off/Off5.webp"
        alt="Off5"
      />
      <img
        class="rounded-xl lg:rounded-2xl col-span-6"
        src="/public/img/off/Off4.webp"
        alt="Off4"
      />
      <img
        class="rounded-xl lg:rounded-2xl col-span-6"
        src="/public/img/off/Off1.webp"
        alt="Off1"
      />
      <img
        class="rounded-xl lg:rounded-2xl col-span-6 -mt-[15vw] md:-mt-[12.3vw] xl:-mt-[9.5vw]"
        src="/public/img/off/Off2.webp"
        alt="Off2"
      />
      <img
        class="rounded-xl lg:rounded-2xl col-span-12"
        src="/public/img/off/Off3.webp"
        alt="Off3"
      />
    </div>

    <div class="w-11/12 lg:w-10/12 mx-auto border-1 rounded-2xl mb-24 lg:mb-32"></div>

    <div class="mb-12 lg:mb-20">
      <h4 class="text-(--color-Rouge) mb-4">
        Vitra Design Museum – À la découverte du design et de l’architecture
      </h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Une immersion d’une journée dans l’un des plus prestigieux musées du design européen
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Le Vitra Design Museum, situé à Weil am Rhein en Allemagne, est l’un des musées les plus
        prestigieux consacrés au design et à l’architecture. Il présente une collection
        exceptionnelle de meubles iconiques, de prototypes et d’objets signés par les plus grands
        designers comme Charles & Ray Eames, Jean Prouvé, Verner Panton et Zaha Hadid.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Cette sortie d’une journée, réservée aux étudiants de 2ème année, permet de découvrir
        l’histoire et l’évolution du design à travers des expositions immersives et des
        installations interactives. Les étudiants visitent également le campus Vitra, un site
        architectural unique conçu par des architectes renommés.
      </p>
    </div>

    <VideoPlayer
      videoSrc="/video/Vitra.mp4"
      videoClasses="rounded-xl lg:rounded-2xl mb-12 lg:mb-20"
    />

    <div class="mb-12 lg:mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Qui peut y participer ?</h4>
      <ul class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        <li>
          Sortie réservée aux étudiants de 2ème année, organisée pour découvrir les icônes du design
          et comprendre leur impact sur notre quotidien.
        </li>
      </ul>
    </div>
    <div class="mb-12 lg:mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Pourquoi y aller ?</h4>
      <ul class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        <li>Explorer des pièces de mobilier et objets de design ayant marqué l’histoire.</li>
        <li>
          Comprendre les processus de création et d’innovation à travers des expositions
          interactives.
        </li>
        <li>
          Visiter le campus Vitra, un site architectural unique avec des bâtiments conçus par des
          architectes mondialement reconnus.
        </li>
      </ul>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Une visite essentielle pour mieux comprendre les fondamentaux du design et de l’ergonomie !
      </p>
    </div>

    <div class="grid grid-cols-12 gap-2 lg:gap-5 mb-44 lg:mb-76">
      <img
        class="rounded-xl lg:rounded-2xl col-span-6"
        src="/public/img/Vitra/Vitra2.webp"
        alt="Vitra2"
      />
      <img
        class="rounded-xl lg:rounded-2xl col-span-6"
        src="/public/img/Vitra/Vitra3.webp"
        alt="Vitra3"
      />

      <!-- Image 3 avec h-full et object-cover -->
      <img
        class="rounded-xl lg:rounded-2xl col-span-4 h-full object-cover"
        src="/public/img/Vitra/Vitra1.webp"
        alt="Vitra1"
      />

      <!-- Image 4 avec h-full pour qu'elles soient de même hauteur -->
      <img
        class="rounded-xl lg:rounded-2xl col-span-8 h-full"
        src="/public/img/Vitra/Vitra4.webp"
        alt="Vitra4"
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
