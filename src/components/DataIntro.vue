<template>
  <section class="relative overflow-hidden py-20 my-4 lg:my-20">
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
          <h3 ref="counter1">0</h3>
          <h6>
            Étudiants et personnels français en mobilité Erasmus+ sont partis étudier dans les pays
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
          <h3 ref="counter2">0</h3>
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
          <div class="flex items-center justify-center space-x-2">
          <h3>+</h3><h3 ref="counter3"> 0 </h3>
        </div>
          <h6>Nombre de pays accessibles via les programmes d’échange</h6>
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
          <h3 ref="counter4">0</h3>
          <h6>
            Nombre d’accords de partenariat signés entre les IUT français et des établissements d'enseignement supérieur en Europe
          </h6>
        </div>
        <div
          class="bg-(--color-Blanc)/50 text-(--color-Noir) text-center drop-shadow-lg backdrop-blur-xl rounded-xl p-8 px-3 md:px-10 lg:p-10 lg:px-6 col-span-6 lg:col-span-3 lg:rounded-3xl"
        >
        <div class="flex items-center justify-center space-x-2">
          <h3 ref="counter5"> 0 </h3><h3>%</h3>
        </div>

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
          <div class="flex items-center justify-center space-x-2">
          <h3 ref="counter6"> 0 </h3><h3>€</h3>
        </div>
          <h6>
            Montant moyen des aides financières disponibles pour une mobilité d’un an (bourses Erasmus+, AMI, Régions)
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
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue';
import { gsap } from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
import CarteIcon from '@/components/icons/CarteIcon.vue';

gsap.registerPlugin(ScrollTrigger);

const counter1 = ref<HTMLElement | null>(null);
const counter2 = ref<HTMLElement | null>(null);
const counter3 = ref<HTMLElement | null>(null);
const counter4 = ref<HTMLElement | null>(null);
const counter5 = ref<HTMLElement | null>(null);
const counter6 = ref<HTMLElement | null>(null);

onMounted(() => {
  const counters = [counter1, counter2, counter3, counter4, counter5, counter6];
  counters.forEach((counterRef, index) => {
    const counter = counterRef.value;
    if (counter) {
      gsap.fromTo(
        counter,
        { innerText: 0 },
        {
          innerText: getTargetValue(index),
          duration: 2,
          scrollTrigger: {
            trigger: counter,
            start: 'top 80%',
            toggleActions: 'play none none reverse',
            once: true, // Assure que l'animation ne se déclenche qu'une seule fois
          },
          ease: 'power1.inOut',
          onUpdate: () => {
            counter.innerText = Math.ceil(gsap.getProperty(counter, 'innerText')).toString();
          },
        }
      );
    }
  });


});

const getTargetValue = (index: number): number => {
  switch (index) {
    case 0:
      return 53000;
    case 1:
      return 378;
    case 2:
      return 30;
    case 3:
      return 1700;
    case 4:
      return 16;
    case 5:
      return 8500;
    default:
      return 0;
  }
};

</script>
