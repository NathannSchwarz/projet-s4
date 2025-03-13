<script setup lang="ts">
import { ref } from "vue";
import { useRoute, useRouter } from "vue-router";

const isMenuOpen = ref(false);
const route = useRoute();
const router = useRouter();

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

// Vérifier si une route est active
const isActive = (path: string) => route.path === path;

// Fermer le menu lorsqu'un lien est cliqué
const closeMenu = (path: string) => {
  if (route.path !== path) {
    isMenuOpen.value = false;
    router.push(path);
  }
};

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: "smooth" });
};
</script>

<template>
  <header
    class="fixed top-0 left-1/2 -translate-x-1/2 z-50 mt-5 lg:mt-8 w-11/12 md:w-10/12 mx-auto bg-(--color-Jaune) flex items-center justify-between lg:justify-around p-4 font-roboto"
    :class="{ 'rounded-xl md:rounded-2xl': !isMenuOpen, 'rounded-t-xl lg:rounded-2xl': isMenuOpen }"
  >
    <!-- Zone gauche : Logos -->
    <div class="flex items-center gap-2" @click="scrollToTop">
      <router-link to="/" class="flex items-center space-x-4" @click="closeMenu('/') " >
        <img  src="/img/logo/logoprojet1.png" alt="Logo Projet 1" class="h-8 lg:h-10" />
        <img src="/img/logo/logoprojet2.png" alt="Logo Projet 2" class="h-8 lg:h-10" />
      </router-link>
    </div>

    <!-- Navigation Desktop (au centre, toujours sur une ligne) -->
    <nav class="hidden lg:flex items-center gap-4 text-(--color-Noir)"  @click="scrollToTop">
      <router-link
        to="/stage-europe"
        class="font-semibold relative"
        :class="{ 'underline decoration-2': isActive('/stage-europe') }"
      >
        Stage en Europe
      </router-link>
      <div class="w-2 h-2 bg-(--color-Bleueurope) rounded-full"></div>

      <router-link
        to="/alternance-internationale"
        class="font-semibold relative"
        :class="{ 'underline decoration-2': isActive('/alternance-internationale') }"
      >
        Alternance internationale
      </router-link>
      <div class="w-2 h-2 bg-(--color-Bleueurope) rounded-full"></div>

      <router-link
        to="/sorties-culturelles"
        class="font-semibold relative"
        :class="{ 'underline decoration-2': isActive('/sorties-culturelles') }"
      >
        Sorties culturelles
      </router-link>
    </nav>

    <!-- Zone droite : Logo + Menu Mobile -->
    <div class="flex items-center gap-4">
      <img src="/img/logo/logoprojet4.png" alt="Logo Projet 4" class="h-8 lg:h-10" />

      <!-- Icône de menu Mobile -->
      <button @click="toggleMenu" class="lg:hidden relative w-8 h-3.5 flex flex-col justify-between">
        <span
          class="block w-6 h-[3.5px] bg-(--color-Noir) transition-all duration-300 rounded-full"
          :class="{ 'rotate-45 translate-y-1.5 translate-x-0.5 w-7': isMenuOpen }"
        ></span>
        <span
          class="block w-8 h-[4px] bg-(--color-Noir) transition-all duration-200 rounded-full"
          :class="{ '-rotate-45 -translate-y-1 w-7': isMenuOpen }"
        ></span>
      </button>
    </div>
  </header>

  <!-- Menu Mobile (s'affiche sous le header) -->
  <div
    v-if="isMenuOpen" @click="scrollToTop"
    class="lg:hidden w-11/12 md:w-10/12 mx-auto bg-(--color-Jaune) rounded-b-xl flex flex-col items-center gap-4 py-4 text-(--color-Noir) text-lg fixed top-[83px] left-1/2 -translate-x-1/2 z-50 font-roboto"
  >
    <button @click="closeMenu('/stage-europe')" class="font-semibold">Stage en Europe</button>
    <div class="w-2 h-2 bg-(--color-Bleueurope) rounded-full"></div>
    <button @click="closeMenu('/alternance-internationale')" class="font-semibold">Alternance internationale</button>
    <div class="w-2 h-2 bg-(--color-Bleueurope) rounded-full"></div>
    <button @click="closeMenu('/sorties-culturelles')" class="font-semibold">Sorties culturelles</button>
  </div>
</template>
