<script setup lang="ts">
import VideoPlayer from '@/components/VideoPlayer.vue'
import VideoIntro from '@/components/VideoAccueil.vue'
</script>

<template>
  <VideoIntro
    title="SORTIES"
    subtitle="CULTURELLES"
    videoSrc="/video/OFFVITRA.mp4"
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
      SORTIES
    </h1>

    <!-- Conteneur de la vidéo avec hauteur fixe -->
    <div
      class="relative h-[60vh] overflow-hidden z-20 w-11/12 md:w-9/12 lg:w-5/12 md:-mt-6 xl:-mt-14 lg:h-[45vh] nonevideo"
    >
      <video
        class="absolute top-0 left-1/2 -translate-x-1/2 w-full h-full object-cover rounded-xl xl:rounded-3xl nonevideo no-controls"
        src="/video/OFFVITRA.mp4"
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
        src="/public/img/OFF/OFF7.webp"
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
        src="/public/img/OFF/OFF6.webp"
        alt="Off6"
      />
    </div>

    <div class="w-11/12 lg:w-10/12 mx-auto border-1 rounded-2xl mb-24 lg:mb-32"></div>

    <div class="mb-12 lg:mb-20 space-y-4">
      <h4 class="text-(--color-Rouge) mb-4">
        OFFF Festival – Plongez au cœur de la création numérique à Barcelone
      </h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Un événement incontournable pour les passionnés de design et d’innovation
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Fondé à Barcelone en 2001,<span class="font-semibold">
          OFFF est le plus grand rassemblement de la créativité contemporaine</span
        >, où les meilleurs talents du monde entier se retrouvent pour partager leur processus de
        création et explorer l’avenir de l’industrie créative mondiale.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        OFFF est un espace dédié à
        <span class="font-semibold"> l’innovation, la collaboration et l’inspiration</span>, mêlant
        icônes établies et nouvelles voix émergentes dans les domaines de l’art, du design et de la
        culture numérique.
      </p>
      <div>
        <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
          Pendant plusieurs jours, le festival propose :
        </p>
        <ul class="ml-4 text-[14px] md:text-[16px] xl:text-[18px] font-poppins font-light">
          <li>
            • Des <span class="font-semibold">conférences inspirantes</span> animées par des figures
            majeures du design et de la communication visuelle.
          </li>
          <li>
            • Des <span class="font-semibold"> ateliers pratiques</span> et
            <span class="font-semibold">masterclasses</span> pour expérimenter de nouvelles
            approches créatives.
          </li>
          <li>
            • Des <span class="font-semibold">installations et expositions immersives</span> mettant
            en avant les nouvelles tendances du digital.
          </li>
          <li>
            • Un <span class="font-semibold"> marché du design</span> où découvrir les œuvres et
            productions des artistes présents.
          </li>
        </ul>
      </div>

      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Depuis plus de 25 ans, OFFF s’engage à rassembler <span class="font-semibold">les leaders du graphisme, les artistes du
        digital, les pionniers de l’interactivité et les esprits visionnaires</span>. Il attire une
        communauté mondiale de créatifs, designers, artistes, développeurs et passionnés de
        technologie, mode et communication.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Bien que l’événement principal ait lieu <span class="font-semibold">chaque printemps à Barcelone</span> , OFFF organise aussi
        des éditions dans des villes comme Séville, Mexico, Vienne, Tel Aviv et bien d’autres.
      </p>
    </div>

    <VideoPlayer
      videoSrc="/video/Off.mp4"
      videoClasses="rounded-xl lg:rounded-2xl mb-12 lg:mb-20"
    />

    <div class="mb-12 lg:mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Qui peut y participer ?</h4>
      <ul class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins font-light  ml-2 lg:ml-3">
        <li>•<span class="font-semibold"> 1ère année </span>: Accessible aux meilleurs étudiants du classement.</li>
        <li>•<span class="font-semibold"> 2ème & 3ème année </span>: Ouvert aux alternants, sur proposition des enseignants.</li>
      </ul>
    </div>
    <div class="mb-12 lg:mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Pourquoi y aller ?</h4>
      <ul class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins mb-6 font-light  ml-2 lg:ml-3">
        <li>
          • Assister à des <span class="font-semibold">conférences inspirantes</span> de designers, directeurs artistiques et studios
          renommés.
        </li>
        <li>• Découvrir <span class="font-semibold">les dernières tendances</span>  du design interactif et du branding digital.</li>
        <li>• Rencontrer des professionnels et <span class="font-semibold">élargir son réseau</span> pour son avenir.</li>
      </ul>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Un véritable tremplin pour booster sa créativité et son inspiration !
      </p>
    </div>

    <div class="grid grid-cols-12 gap-2 lg:gap-5 mb-24 lg:mb-32">
      <img
        class="rounded-xl lg:rounded-2xl col-span-6"
        src="/public/img/OFF/OFF5.webp"
        alt="Off5"
      />
      <img
        class="rounded-xl lg:rounded-2xl col-span-6"
        src="/public/img/OFF/OFF4.webp"
        alt="Off4"
      />
      <img
        class="rounded-xl lg:rounded-2xl col-span-6"
        src="/public/img/OFF/OFF1.webp"
        alt="Off1"
      />
      <img
        class="rounded-xl lg:rounded-2xl col-span-6 -mt-[15vw] md:-mt-[12.3vw] xl:-mt-[9.5vw]"
        src="/public/img/OFF/OFF2.webp"
        alt="Off2"
      />
      <img
        class="rounded-xl lg:rounded-2xl col-span-12"
        src="/public/img/OFF/OFF3.webp"
        alt="Off3"
      />
    </div>

    <div class="w-11/12 lg:w-10/12 mx-auto border-1 rounded-2xl mb-24 lg:mb-32"></div>

    <div class="mb-12 lg:mb-20 space-y-4">
      <h4 class="text-(--color-Rouge) mb-4">
        Vitra Design Museum – À la découverte du design et de l’architecture
      </h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Une immersion d’une journée dans l’un des plus prestigieux musées du design européen.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Le <span class="font-semibold">Vitra Design Museum</span> , situé à Weil am Rhein en Allemagne, est l’un des musées les plus
        prestigieux consacrés au design et à l’architecture. Il présente <span class="font-semibold">une collection
        exceptionnelle de meubles iconiques</span> , de prototypes et d’objets signés par les plus grands
        designers comme <span class="font-semibold">Charles & Ray Eames, Jean Prouvé, Verner Panton et Zaha Hadid</span> .
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Cette sortie d’une journée, réservée aux <span class="font-semibold">étudiants de 2ème année</span> , permet de découvrir
        l’histoire et l’évolution du design à travers <span class="font-semibold">des expositions immersives et des
        installations interactives</span> . Les étudiants visitent également <span class="font-semibold">le campus Vitra</span> , un site
        architectural unique conçu par des architectes renommés.
      </p>
    </div>

    <VideoPlayer
      videoSrc="/video/Vitra.mp4"
      videoClasses="rounded-xl lg:rounded-2xl mb-12 lg:mb-20"
    />

    <div class="mb-12 lg:mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Qui peut y participer ?</h4>
      <ul class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins font-light  ml-2 lg:ml-3">
        <li>
         •  <span class="font-semibold"> Sortie réservée aux étudiants de 2ème année</span>, organisée pour découvrir les icônes du design
          et comprendre leur impact sur notre quotidien.
        </li>
      </ul>
    </div>
    <div class="mb-12 lg:mb-20">
      <h4 class="text-(--color-Rouge) mb-4">Pourquoi y aller ?</h4>
      <ul class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins mb-6 font-light ml-2 lg:ml-3">
        <li>• Explorer <span class="font-semibold">des pièces de mobilier</span>  et <span class="font-semibold">objets de design</span> ayant marqué l’histoire.</li>
        <li>
          • Comprendre les processus de création et d’innovation à travers <span class="font-semibold">des expositions
          interactives.</span>
        </li>
        <li>
          •  Visiter <span class="font-semibold">le campus Vitra</span> , un site architectural unique avec des bâtiments conçus par des
          architectes mondialement reconnus.
        </li>
      </ul>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Une visite essentielle pour mieux comprendre les fondamentaux du design et de l’ergonomie !
      </p>
    </div>

    <div class="grid grid-cols-12 gap-2 lg:gap-5 mb-40 lg:mb-70">
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
