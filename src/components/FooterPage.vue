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
  window.scrollTo({ top: 0, behavior: "smooth" });
};
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

        <section class="grid grid-cols-2 md:grid-cols-3 gap-3.5 xl:gap-10 mt-10 lg:mt-20 pb-32 xl:pb-56">
          <div
            v-for="(card, index) in [
              {
                icon: SchoolIcon,
                title: 'CANDIDATER',
                text: 'Pour partir à l’étranger via le MMi, il faut suivre plusieurs étapes',
                color: '--color-Jaune',
              },
              {
                icon: EuroIcon,
                title: 'AIDES FINANCIÈRES',
                text: 'Il existe plusieurs bourses pour financer votre mobilité',
                color: '--color-Rouge',
              },
              {
                icon: PlaneIcon,
                title: 'DESTINATION',
                text: 'Le choix de la destination dépend de plusieurs critères',
                color: '--color-Turquoise',
              },
              {
                icon: StagesIcon,
                title: 'RECHERCHE STAGES',
                text: 'Trouver une entreprise pour mon stage en Europe',
                color: '--color-Jaune',
              },
              {
                icon: InscriptionIcon,
                title: 'INSCRIPTION SORTIES',
                text: 'S’inscrire aux sorties internationales proposées',
                color: '--color-Rouge',
              },
              {
                icon: CheckIcon,
                title: 'POURQUOI L’EUROPE',
                text: 'Les avantages d’une alternance internationale',
                color: '--color-Turquoise',
              },
            ]"
            :key="index"
            class="text-(--color-Blanc) bg-(--color-Blanc)/30 backdrop-blur-lg rounded-2xl flex flex-col justify-center items-center text-center transition-all duration-500 space-y-2 xl:space-y-3 font-poppins"
            :class="
              activeCard === index
                ? 'col-span-2 md:col-span-3 p-8 w-full h-full items-start text-left'
                : 'p-4 xl:p-6 items-center text-center'
            "
            v-show="activeCard === null || activeCard === index"
          >
            <!-- Icône (affichée seulement si la carte n'est pas ouverte) -->
            <component :is="card.icon" v-if="activeCard === null" class="lg:h-20 w-24" />

            <h5>{{ card.title }}</h5>
            <p class="text-[12px] lg:text-[14px] xl:text-[15px]">
              {{ card.text }}
            </p>

            <!-- Bouton Voir plus / Fermer -->
            <button
              class="text-[12px] font-semibold font-poppins lg:text-[16px] flex items-center gap-3 p-1 px-6 rounded-lg self-center cursor-pointer"
              :style="{ backgroundColor: `var(${card.color})` }"
              @click="activeCard === index ? resetGrid() : expandCard(index)"
            >
              {{ activeCard === index ? 'Fermer' : 'Voir plus' }}
              <ArrowIcon v-if="activeCard === null" />
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
          <ul class="flex space-x-8 space-y-5">
            <li><img class="h-8 lg:h-10" src="/img/logo/logoprojet1.png" alt="" /></li>
            <li><img class="h-8 lg:h-10" src="/img/logo/logoprojet2.png" alt="" /></li>
            <li><img class="h-8 lg:h-10" src="/img/logo/logoprojet5.png" alt="" /></li>
          </ul>
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
          <ul class="space-y-2  font-roboto font-light text-sm " @click="scrollToTop">
            <li class="hover:font-semibold transition-all duration-300"><router-link  to="stage-europe " >Stages en Europe</router-link></li>
            <li class="hover:font-semibold transition-all duration-300"><router-link to="alternance-internationale">Alternances Internationale</router-link></li>
            <li class="hover:font-semibold transition-all duration-300"><router-link to="sorties-culturelles">Sorties Culturelles</router-link></li>
          </ul>
        </div>

        <div class="space-y-3 col-span-2 md:col-span-4 lg:col-span-3" @click="scrollToTop">
          <h5>INFORMATIONS LÉGALES</h5>
          <ul class="space-y-2 font-roboto font-light text-sm">
            <li class="hover:font-semibold transition-all duration-300"><a href="https://www.iut-nfc.univ-fcomte.fr/plans/" target="_blank">Accès à nos sites formation</a></li>
            <li class="hover:font-semibold transition-all duration-300"><router-link to="#">Mentions légales</router-link></li>
            <li class="hover:font-semibold transition-all duration-300"><router-link to="#">Politiques de cookies (EU)</router-link></li>
          </ul>
        </div>

        <!-- Bloc Réseaux Sociaux -->
        <div class="space-y-3 col-span-4 md:col-span-2 lg:col-span-3">
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
      </section>
    </div>
  </footer>
</template>
