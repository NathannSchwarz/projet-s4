<script setup lang="ts">
import CheckIcon from '@/components/icons/CheckIcon.vue'
import EuroIcon from '@/components/icons/EuroIcon.vue'
import InscriptionIcon from '@/components/icons/InscriptionIcon.vue'
import SchoolIcon from '@/components/icons/SchoolIcon.vue'
import StagesIcon from '@/components/icons/StagesIcon.vue'
import PlaneIcon from '@/components/icons/PlaneIcon.vue'
import ArrowIcon from '@/components/icons/ArrowIcon.vue'

import { ref } from 'vue'

const activeCard = ref<number | null>(null)

// Fonction pour activer une carte
const expandCard = (index: number) => {
  activeCard.value = index

  // Vérifier si l'élément existe avant d'appliquer le scroll
  const section = document.getElementById('faq-section')
  if (section) {
    section.scrollIntoView({ behavior: 'smooth', block: 'start' })
  }
}

// Fonction pour réinitialiser (fermer la carte)
const resetGrid = () => {
  activeCard.value = null
}

const scrollToTop = () => {
  window.scrollTo(0, 0)
}

// Définition du type pour chaque carte
interface Card {
  icon: any
  title: string
  text: string
  description: string
  color: string
}

// Déclaration des cartes avec un typage strict
const cards: Readonly<Card[]> = [
  {
    icon: SchoolIcon,
    title: 'CANDIDATER',
    text: 'Pour partir à l’étranger via le MMi, il faut suivre plusieurs étapes',
    description: `
    <p>Pour effectuer une <span class="!font-semibold">mobilité internationale</span> avec le <span class="!font-semibold">BUT MMI</span>, il est essentiel de suivre un processus précis :</p>
    <ul class="list-disc ml-5 mt-2">
      <li><span class="!font-semibold">Se renseigner</span> : Découvrez les opportunités <i>(stages, échanges académiques, alternances)</i> et les destinations disponibles.</li>
      <li><span class="!font-semibold">Préparer son dossier</span> : Inclut un <span class="!font-semibold">CV</span>, une <span class="!font-semibold">lettre de motivation</span> et un <span class="!font-semibold">portfolio</span> si nécessaire.</li>
      <li><span class="!font-semibold">Respecter les prérequis</span> : Certaines destinations exigent un <i>niveau de langue spécifique</i> ou un <i>entretien</i>.</li>
      <li><span class="!font-semibold">Finaliser les démarches administratives</span> : Convention de stage, inscription à l’université partenaire, visa.</li>
    </ul>
  `,
    color: '--color-Jaune',
  },

  {
    icon: EuroIcon,
    title: 'AIDES FINANCIÈRES',
    text: 'Il existe plusieurs bourses pour financer votre mobilité',
    description: `
    <p>Pour <span class="!font-semibold">alléger les coûts</span> de votre mobilité, plusieurs aides sont disponibles :</p>
    <ul class="list-disc ml-5 mt-2">
      <li><span class="!font-semibold">Erasmus+</span> : Une bourse couvrant une partie des frais de séjour en Europe.</li>
      <li><span class="!font-semibold">Aide à la Mobilité Internationale (AMI)</span> : Une aide de l'État pour les étudiants en stage ou échange.</li>
      <li><span class="!font-semibold">Aides régionales et départementales</span> : Variable selon votre lieu de résidence.</li>
      <li><span class="!font-semibold">Bourses d’entreprises et fondations</span> : Certaines entreprises offrent des subventions aux étudiants.</li>
    </ul>
    <p class="mt-2">Renseignez-vous auprès du <span class="!font-semibold">service des relations internationales</span> de votre IUT pour connaître les critères d’éligibilité.</p>
  `,
    color: '--color-Rouge',
  },

  {
    icon: PlaneIcon,
    title: 'DESTINATION',
    text: 'Le choix de la destination dépend de plusieurs critères',
    description: `
    <p>Le choix de votre destination dépend de plusieurs critères :</p>
    <ul class="list-disc ml-5 mt-2">
      <li><span class="!font-semibold">Projet professionnel</span> : Optez pour un pays en lien avec votre futur métier.</li>
      <li><span class="!font-semibold">Niveau de langue</span> : Vérifiez si un test de langue est requis.</li>
      <li><span class="!font-semibold">Coût de la vie</span> : Prenez en compte le logement, la nourriture et les transports.</li>
      <li><span class="!font-semibold">Facilité administrative</span> : Erasmus+ simplifie les échanges en Europe, hors UE les démarches sont plus complexes.</li>
    </ul>
    <p class="mt-2">Pensez aussi à vérifier la <span class="!font-semibold">reconnaissance des diplômes</span> et l’environnement culturel.</p>
  `,
    color: '--color-Turquoise',
  },

  {
    icon: StagesIcon,
    title: 'RECHERCHE STAGES',
    text: 'Trouver une entreprise pour mon stage en Europe',
    description: `
    <p>Un stage à l’étranger demande de l’anticipation :</p>
    <ul class="list-disc ml-5 mt-2">
      <li><span class="!font-semibold">Cibler les secteurs d’intérêt</span> et repérer les entreprises internationales.</li>
      <li><span class="!font-semibold">Utiliser les bonnes plateformes</span> : <i>ErasmusIntern, LinkedIn, chambres de commerce françaises</i>.</li>
      <li><span class="!font-semibold">Activer son réseau</span> : Professeurs, anciens étudiants, relations professionnelles.</li>
      <li><span class="!font-semibold">Adapter son CV et sa lettre de motivation</span> aux standards du pays.</li>
    </ul>
    <p class="mt-2">Pensez à préparer un <span class="!font-semibold">entretien en visio</span> si nécessaire.</p>
  `,
    color: '--color-Jaune',
  },

  {
    icon: InscriptionIcon,
    title: 'INSCRIPTION SORTIES',
    text: 'S’inscrire aux sorties internationales proposées',
    description: `
    <p>Votre établissement organise des événements en lien avec la <span class="!font-semibold">mobilité internationale</span> :</p>
    <ul class="list-disc ml-5 mt-2">
      <li><span class="!font-semibold">Voyages d’études</span> vers des universités partenaires.</li>
      <li><span class="!font-semibold">Rencontres</span> avec des étudiants étrangers.</li>
      <li><span class="!font-semibold">Forums et conférences</span> sur la mobilité.</li>
    </ul>
    <p class="mt-2">L’inscription se fait via un <span class="!font-semibold">formulaire en ligne</span> ou auprès du <span class="!font-semibold">service des relations internationales</span>.</p>
  `,
    color: '--color-Rouge',
  },

  {
    icon: CheckIcon,
    title: 'POURQUOI L’EUROPE',
    text: 'Les avantages d’une alternance internationale',
    description: `
    <p>Choisir l’Europe pour une <span class="!font-semibold">alternance internationale</span> offre de nombreux avantages :</p>
    <ul class="list-disc ml-5 mt-2">
      <li><span class="!font-semibold">Immersion professionnelle</span> dans un environnement international.</li>
      <li><span class="!font-semibold">Amélioration des compétences linguistiques</span>.</li>
      <li><span class="!font-semibold">Valorisation du CV</span> auprès des employeurs.</li>
    </ul>
    <p class="mt-2">Grâce à <span class="!font-semibold">Erasmus+</span>, la reconnaissance académique et administrative est facilitée.</p>
  `,
    color: '--color-Turquoise',
  },
]
</script>
<template>
  <div class="h-40 bg-gradient-to-b from-(--color-Blanc) to-(--color-Bleueurope)"></div>
  <footer>
    <div class="bg-(--color-Bleueurope) relative overflow-hidden">
      <img
        class="absolute left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 rotate-90 md:rotate-0 w-auto max-w-none h-[85vh] xl:h-[110vh]"
        src="/img/bgfooter.webp"
        alt="bgfooter"
      />
      <section id="faq-section" class="w-11/12 md:w-9/12 xl:w-7/12 mx-auto">
        <div class="pt-32 xl:pt-56">
          <h4 class="text-(--color-Blanc) mb-3 lg:mb-4">
            FAQ – Tout savoir sur votre mobilité internationale
          </h4>
          <p class="text-(--color-Blanc) text-[14px] md:text-[16px] xl:text-[18px] font-poppins">
            Vous envisagez un stage, un échange ou une alternance à l’étranger, mais vous avez
            encore des questions ? Notre FAQ est là pour vous guider ! <br /><br />
            Que ce soit pour trouver la bonne destination, comprendre les démarches administratives,
            obtenir des aides financières ou organiser votre logement, cette section répond aux
            interrogations les plus fréquentes des étudiants du MMi.
          </p>
        </div>

        <section
          class="grid grid-cols-2 md:grid-cols-3 gap-3.5 xl:gap-10 mt-10 lg:mt-20 pb-32 xl:pb-56"
        >
          <div
            v-for="(card, index) in cards"
            :key="card.title"
            class="text-(--color-Blanc) bg-(--color-Blanc)/30 backdrop-blur-lg rounded-2xl flex flex-col justify-center items-center text-center transition-all duration-500 space-y-2 xl:space-y-3 font-poppins"
            :class="
              activeCard === index
                ? 'col-span-2 md:col-span-3 p-8 w-full h-full items-start text-left'
                : 'p-4 xl:p-6 items-center text-center'
            "
            v-show="activeCard === null || activeCard === index"
          >
            <!-- Icône uniquement si la carte est fermée -->
            <component :is="card.icon" v-if="activeCard === null" class="lg:h-20 w-24" />

            <h5>{{ card.title }}</h5>

            <p class="text-[12px] lg:text-[14px] xl:text-[15px]">
              {{ card.text }}
            </p>

            <p
              v-if="activeCard === index"
              class="text-[12px] lg:text-[14px] xl:text-[15px] leading-relaxed mt-2"
              v-html="card.description"
            ></p>

            <button
              class="text-[12px] font-semibold font-poppins lg:text-[16px] flex items-center gap-3 p-1 px-6 rounded-lg self-center cursor-pointer transition-all duration-300"
              :class="{ 'mt-3': activeCard === index }"
              :style="{ backgroundColor: `var(${card.color})` }"
              @click="activeCard === index ? resetGrid() : expandCard(index)"
            >
              <template v-if="activeCard === index">
                <ArrowIcon class="rotate-180" />
                Fermer
              </template>
              <template v-else>
                Voir plus
                <ArrowIcon />
              </template>
            </button>
          </div>
        </section>
      </section>
    </div>
    <div class="bg-(--color-Jaune)">
      <section
        class="w-11/12 md:w-9/12 mx-auto py-20 xl:py-32 grid grid-cols-4 md:grid-cols-6 lg:grid-cols-12 gap-6 md:gap-8 lg:gap-10"
      >
        <!-- Bloc Informations -->
        <div class="space-y-3 col-span-4 lg:col-span-4">
          <h5>INFORMATIONS</h5>

          <p class="font-roboto text-sm">
            iUT Nord Franche-Comté <br />
            19 avenue du Maréchal Juin <br />
            BP 527 <br />
            90016 Belfort Cedex
          </p>
          <p class="!font-semibold font-roboto text-sm">+33 (0)3 84 58 77 00</p>
          <p class="font-roboto text-sm">
            L’iUT Nord Franche-Comté est une composante de l’Université Marie et Louis Pasteur.
            Établissement public d’enseignement supérieur.
          </p>
        </div>

        <div class="space-y-3 col-span-2">
          <h5>MENU</h5>
          <ul class="space-y-2 font-roboto font-light text-sm" @click="scrollToTop">
            <li class="hover:font-semibold transition-all duration-300">
              <router-link to="/StagePage">Stages en Europe</router-link>
            </li>
            <li class="hover:font-semibold transition-all duration-300">
              <router-link to="/SortiesPage">Sorties Culturelles</router-link>
            </li>
            <li class="hover:font-semibold transition-all duration-300">
              <router-link to="/AlternancePage">Alternances en Europe</router-link>
            </li>
          </ul>
        </div>

        <div class="space-y-3 col-span-2 md:col-span-4 lg:col-span-3" @click="scrollToTop">
          <h5>INFORMATIONS LÉGALES</h5>
          <ul class="space-y-2 font-roboto font-light text-sm">
            <li class="hover:font-semibold transition-all duration-300">
              <a href="https://www.iut-nfc.univ-fcomte.fr/plans/" target="_blank"
                >Accès à nos sites formation</a
              >
            </li>
            <li class="hover:font-semibold transition-all duration-300">
              <router-link to="#">Mentions légales</router-link>
            </li>
            <li class="hover:font-semibold transition-all duration-300">
              <router-link to="#">Politiques de cookies (EU)</router-link>
            </li>
          </ul>
        </div>

        <!-- Bloc Réseaux Sociaux -->
        <div class="space-y-3 col-span-4 md:col-span-2 lg:col-span-3 space-y-16 xl:space-y-24">
          <div class="space-y-3">
            <h5>RÉSEAUX SOCIAUX</h5>
            <ul class="flex space-x-3">
              <li>
                <a href="#" target="_blank"
                  ><img class="h-7 lg:h-8" src="/img/social/instagram.png" alt="Instagram"
                /></a>
              </li>
              <li>
                <a href="#" target="_blank"
                  ><img class="h-7 lg:h-8" src="/img/social/facebook.png" alt="Facebook"
                /></a>
              </li>
              <li>
                <a href="#" target="_blank"
                  ><img class="h-7 lg:h-8" src="/img/social/ytb.png" alt="YouTube"
                /></a>
              </li>
              <li>
                <a href="#" target="_blank"
                  ><img class="h-7 lg:h-8" src="/img/social/linkedin.png" alt="LinkedIn"
                /></a>
              </li>
              <li>
                <a href="#" target="_blank"
                  ><img class="h-7 lg:h-8" src="/img/social/tiktok.png" alt="TikTok"
                /></a>
              </li>
            </ul>
          </div>

          <ul class="flex space-x-8  items-center justify-center align-center xl:justify-start">
            <li><img class="h-8 lg:h-10" src="/img/logo/logoprojet1.png" alt="" /></li>
            <li><img class="h-8 lg:h-10" src="/img/logo/logoprojet7.png" alt="" /></li>
            <li><img class="h-8 lg:h-10" src="/img/logo/logoprojet5.png" alt="" /></li>
          </ul>
        </div>
      </section>
    </div>
  </footer>
</template>
