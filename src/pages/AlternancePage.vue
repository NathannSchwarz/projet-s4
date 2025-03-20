<script setup lang="ts">
import VideoPlayer from '@/components/VideoPlayer.vue'
import Alternance1 from '@/components/icons/Alternance1.vue'
import Alternance2 from '@/components/icons/Alternance2.vue'
import Alternance3 from '@/components/icons/Alternance3.vue'
import Alternance4 from '@/components/icons/Alternance4.vue'
import Earth from '@/components/icons/Earth.vue'
import VideoIntro from '@/components/VideoAccueil.vue'
import { useHead } from '@unhead/vue'

const scrollToTop = () => {
  window.scrollTo(0, 0);
}

import { onMounted } from 'vue'

onMounted(() => {
  document.title = 'Alternance en Europe'
})

import { ref, onMounted, computed } from 'vue'

const email = ref('')
const message = ref('')

// Fonction pour envoyer l'email
const submitEmail = () => {
  if (email.value.trim() !== '') {
    message.value = 'Merci ! Vous recevrez bientôt les mises à jour.'
    email.value = '' // Réinitialisation du champ après soumission
  }
}

// Liste des éléments avec images et texte
const items = ref([
  {
    image: '/img/Alternance/Alternance1.webp',
    text: 'Travaillant son CV et sa lettre de motivation en anglais.',
  },
  {
    image: '/img/Alternance/Alternance2.webp',
    text: 'Élargissant son réseau et participer à des événements.',
  },
  {
    image: '/img/Alternance/Alternance3.webp',
    text: 'S’informant sur les entreprises européennes du secteur.',
  },
])

const activeIndex = ref(0) // Premier élément actif par défaut

const toggleActive = (index: number) => {
  if (activeIndex.value !== index) {
    activeIndex.value = index // Change uniquement si c'est un autre élément
  }
}

// Vérifier si on est en mobile (responsive)
const isMobile = computed(() => window.innerWidth < 768)

// Vérifier la taille de l'écran pour réorganiser l'ordre des éléments
onMounted(() => {
  window.addEventListener('resize', () => {
    isMobile.value = window.innerWidth < 768
  })
})


</script>

<template>

   <VideoIntro
    title="ALTERNANCE"
    subtitle="EN EUROPE"
    videoSrc="/video/IUT.mp4"
    class="hidden xl:block"
  />
  <section class="block xl:hidden relative overflow-hidden py-30 xl:py-28 flex flex-col items-center mx-auto">
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

  <section class="w-11/12 md:w-9/12 xl:w-7/12 mx-auto lg:mt-44">
    <div class="mb-20 space-y-4">
      <h4 class="text-(--color-Rouge) mb-4">L’Alternance en Europe – Une opportunité en devenir</h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        L’alternance est <span class="font-semibold">une expérience formatrice</span>  qui permet de combiner études et immersion en
        entreprise. Aujourd’hui, les étudiants du MMi peuvent réaliser leur alternance en France,
        mais une nouvelle opportunité se dessine : <span class="font-semibold">l’alternance en Europe</span> .
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        L’IUT explore actuellement la possibilité de développer <span class="font-semibold">des partenariats avec des
        entreprises européennes</span>  afin de permettre aux étudiants de <span class="font-semibold">réaliser leur alternance à
        l’international</span> , tout en poursuivant leur formation en France.
      </p>
      <p class="text-[16px] md:text-[18px] xl:text-[20px] font-poppins !font-semibold text-(--color-Rouge)">
        Pourquoi envisager une alternance en Europe ?
      </p>
    </div>

    <div class="grid grid-cols-12 grid-row-12 gap-2 text-center lg:gap-5 mb-44 lg:mb-54 ">
      <div
        class="bg-(--color-Jaune) flex flex-col justify-center items-center p-5 md:p-10 gap-5 rounded-xl lg:rounded-2xl col-span-6 row-span-5 shadow-2xl lg:col-span-3 lg:row-span-12  hover:bg-(--color-Noir) hover:text-(--color-Jaune) transition-all duration-500 "
      >
        <Alternance3 class="w-18 xl:w-28" />
        <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins !font-semibold">
          Une expérience professionnelle qui renforce l’employabilité.
        </p>
      </div>

      <div
        class="bg-(--color-Jaune) flex flex-col justify-center items-center p-5 md:p-10 gap-5 rounded-xl lg:rounded-2xl col-span-6 row-span-6 shadow-2xl lg:col-span-9 lg:row-span-5  hover:bg-(--color-Noir) hover:text-(--color-Jaune) transition-all duration-500"
      >
        <Alternance4 class="w-18 xl:w-28" />
        <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins !font-semibold lg:w-2/3 lg:mx-auto">
          Une immersion dans un environnement multiculturel favorisant l’apprentissage des langues.
        </p>
      </div>

      <div
        class="bg-(--color-Jaune) flex flex-col justify-center items-center p-5 md:p-8 gap-5 rounded-xl lg:rounded-2xl col-span-6 row-span-7 shadow-2xl lg:col-span-4 lg:row-span-7  hover:bg-(--color-Noir) hover:text-(--color-Jaune) transition-all duration-500"
      >
        <Alternance2 class="w-18 xl:w-28" />
        <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins !font-semibold">
          L’opportunité de travailler avec des entreprises innovantes et d’élargir son réseau.
        </p>
      </div>

      <div
        class="bg-(--color-Jaune) flex flex-col justify-center items-center p-5 md:p-10 gap-5 rounded-xl lg:rounded-2xl col-span-6 row-span-6 shadow-2xl lg:col-span-5 lg:row-span-7  hover:bg-(--color-Noir) hover:text-(--color-Jaune) transition-all duration-500"
      >
        <Alternance1 class="w-14 xl:w-24" />
        <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins !font-semibold">
          Une valorisation unique sur le CV, recherchée par les recruteurs.
        </p>
      </div>
    </div>

    <div class="space-y-4 mb-44 lg:mb-54 ">
      <h4 class="text-(--color-Rouge) mb-4">Où en est le projet ?</h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        L’alternance à l’étranger est encore en <span class="font-semibold">phase de réflexion</span>  au sein du département MMi. L’IUT
        travaille actuellement à établir <span class="font-semibold">des contacts avec des entreprises et institutions</span>  en
        Europe, dans des secteurs comme :
      </p>
      <ul class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins ml-2 lg:ml-3">
        <li>• <span class="font-semibold">Le design et l’UX/UI</span>  → Studios créatifs en Allemagne, aux Pays-Bas ou en Suède.</li>
        <li>• <span class="font-semibold">Le développement web et numérique</span>  → Startups tech à Barcelone, Berlin ou Amsterdam.</li>
        <li>• <span class="font-semibold">La communication et le marketing digital</span> → Agences à Madrid, Bruxelles ou Milan.</li>
      </ul>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Les enseignants du MMi encouragent déjà les étudiants <span class="font-semibold">à participer à des événements
        internationaux</span> , comme <span class="font-semibold">le OFFF Festival de Barcelone</span><a href="https://www.offf.barcelona/offf-schedule" target="_blank" ><span class="text-(--color-Rouge)"> (voir page dédié)</span></a>   , afin de développer
        leur réseau professionnel et de se préparer à une future expérience en entreprise à
        l’étranger.
      </p>
    </div>

    <div class="mb-44 lg:mb-54 ">
      <h4 class="text-(--color-Rouge) mb-4">Comment se préparer dès maintenant ?</h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins mb-10">
        Même si le programme officiel n’est pas encore lancé, il est possible d’anticiper cette
        opportunité en :
      </p>

      <div class="grid grid-cols-2 md:grid-cols-9 gap-4 transition-all duration-500 ">
        <div
          v-for="(item, index) in items"
          :key="index"
          class="relative transition-all duration-500 ease-in-out flex flex-col items-center justify-center overflow-hidden cursor-pointer rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px]"
          :class="{
            'col-span-2 order-first md:order-none': activeIndex === index && isMobile, // En mobile, élément actif en haut
            'col-span-1 md:col-span-2': activeIndex !== index,
            'col-span-2 md:col-span-5': activeIndex === index,
          }"
          @click="toggleActive(index)"
        >
          <!-- Image -->
          <img
            :src="item.image"
            :alt="'Alternance' + (index + 1)"
            class="w-full h-40 lg:h-56 object-cover transition-all duration-500"
          />

          <!-- Overlay pour l'élément actif -->
          <div
            v-if="activeIndex === index"
            class="absolute inset-0 bg-black/80 gap-10 flex items-center justify-center text-white p-10 transition-opacity duration-300 rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px]"
          >
            <Earth class="w-24" />
            <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins !font-semibold">
              {{ item.text }}
            </p>
          </div>
        </div>
      </div>
    </div>

    <div class="mb-44 lg:mb-54 ">
      <h4 class="text-(--color-Rouge) mb-4">Restez informé sur l’évolution du projet !</h4>

      <div
        class="flex flex-col items-center space-y-6 bg-(--color-Turquoise) p-8 lg:py-14 shadow-2xl mx-auto rounded-tl-[70px] rounded-tr-[10px] rounded-bl-[10px] rounded-br-[70px] lg:rounded-tl-[80px] lg:rounded-tr-[20px] lg:rounded-bl-[20px] lg:rounded-br-[80px]"
      >
        <!-- Image et Texte -->
        <div class="grid grid-cols-8 flex justify-center items-center">
          <img
            class="mx-auto w-40 md:w-44 xl:w-56 col-span-8 md:col-span-3"
            src="/public/img/logo/logoprojet1.png"
            alt="Logo"
          />
          <div class="mt-4 text-[14px] md:text-[16px] xl:text-[18px] col-span-8 md:col-start-4 md:col-span-4 space-y-2 lg:space-y-3">
            <p

          >
            L’avenir de votre formation pourrait bientôt s’écrire à l’international. Soyez prêts à
            saisir cette opportunité !
          </p>
          <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins !font-semibold"> Si vous êtes intéressé et souhaitez être parmi les premiers à
            en bénéficier, inscrivez-vous pour recevoir les mises à jour !</p>

          </div>


        </div>

        <!-- Formulaire -->
        <form @submit.prevent="submitEmail" class="w-full md:w-4/5 flex flex-col items-center">
          <input
            v-model="email"
            type="email"
            placeholder="Inscrivez votre email :)"
            class="w-full px-4 py-2 border text-center shadow-sm focus:outline-none focus:ring-2 focus:ring-(--color-Jaune) rounded-tl-[30px] rounded-tr-[10px] lg:rounded-tl-[40px] lg:rounded-tr-[20px]"
            required
          />
          <button
            type="submit"
            class="w-full bg-black text-white py-2 border-black border-b-1 border-r-1 border-l-1 hover:bg-(--color-Jaune) transition duration-300 rounded-bl-[10px] rounded-br-[30px] hover:text-black lg:rounded-bl-[20px] lg:rounded-br-[40px]"
          >
            S'inscrire
          </button>

          <!-- Message de confirmation -->
          <p v-if="message" class="text-(--color-Bleu) font-semibold">{{ message }}</p>
        </form>
      </div>
    </div>
  </section>

  <section class="w-11/12 md:w-9/12 xl:w-7/12 mx-auto">
    <div class="mb-20 space-y-4">
      <h4 class="text-(--color-Rouge) mb-4">
        Stages à l’étranger : une inspiration pour les futurs alternants
      </h4>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        Nos anciens étudiants ont vécu des stages en Europe, découvrant de nouvelles méthodes de
        travail, développant leurs compétences et élargissant leur réseau. Leurs expériences offrent
        <span class="font-semibold">un aperçu concret de ce que pourrait être l’alternance à l’international</span>, une opportunité en
        cours de développement au MMi.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
        De Berlin à Barcelone, ces témoignages montrent à quel point<span class="font-semibold">travailler à l’étranger est un
        atout</span> . L’alternance en Europe suivra cette dynamique, combinant études et immersion
        professionnelle.
      </p>
      <p class="text-[14px] md:text-[16px] xl:text-[18px] font-poppins !font-semibold">
        Découvrez leurs parcours et projetez-vous dans votre futur à l’international !
      </p>
    </div>

    <div
      class="p-5 py-7 lg:p-10 lg:py-7 bg-gradient-to-b from-[var(--color-Rouge)] to-[var(--color-Blanc)] lg:bg-gradient-to-r lg:from-[var(--color-Rouge)] lg:to-[var(--color-Blanc)] text-(--color-Blanc) grid grid-cols-1 lg:grid-cols-9 gap-5 lg:gap-8 lg:items-center lg:justify-center inset-shadow-md rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[20px] lg:rounded-tr-[80px] lg:rounded-bl-[80px] lg:rounded-br-[20px] mb-20 lg:mb-40"
    >
      <!-- Conteneur des textes -->
      <div class="space-y-3 lg:col-span-3">
        <h4 class="lg:mb-5">Stage en UX/UI design à Berlin</h4>
        <p class="text-[16px] md:text-[18px] xl:text-[20px] font-poppins !font-semibold">
         Loïc MATTERN
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
      class="p-5 py-7 lg:p-10 lg:py-7 bg-gradient-to-b from-[var(--color-Jaune)] to-[var(--color-Blanc)] lg:bg-gradient-to-r lg:from-[var(--color-Blanc)] lg:to-[var(--color-Jaune)] text-(--color-Blanc) grid grid-cols-1 lg:grid-cols-9 gap-5 lg:gap-6 lg:items-center lg:justify-center inset-shadow-md rounded-tl-[10px] rounded-tr-[70px] rounded-bl-[70px] rounded-br-[10px] lg:rounded-tl-[80px] lg:rounded-tr-[20px] lg:rounded-bl-[20px] lg:rounded-br-[80px] mb-40 lg:mb-70"
    >
      <!-- Conteneur des textes -->
      <div class="space-y-3 lg:col-span-3 lg:order-2">
        <h4 class="lg:mb-5">Stage en webdesign à Madrid</h4>
        <p class="text-[16px] md:text-[18px] xl:text-[20px] font-poppins !font-semibold">
          Gaëlle GUILLOU
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
