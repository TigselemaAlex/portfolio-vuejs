<script setup lang="ts">

import {ref} from "vue";

const experiences = ref([
  {
    year: "2023",
    title: "Practicante de vinculación",
    business: "Casa de la cultura Núcleo Tungurahua",
    description: "Desarrollo de una aplicación de escritorio para administrar las pinturas del Museo Franklin Ballesteros junto con una API Rest.",
    technologies: [
      "Java",
      "Spring Boot",
      "MySQL",
      "Angular",
      "PrimeNg",
      "PrimeFlex",
      "ElectronJs",
      "Docker"
    ],
  },
  {
    year: "2023",
    title: "Practicante de practicas pre-profesionales",
    business: "Posgrados de la Universidad Técnica de Ambato",
    description: "Desarrollo de una aplicación web para el concurso de merecimientos para aspirantes a docentes de la Universidad Técnica de Ambato.",
    technologies: [
      "PHP",
      "Laravel",
      "SQL Server",
      "Livewire",
      "Jetstream",
      "AdminLTE",
      "TailwindCSS",
    ],
  }
])

</script>


<template>
  <section class="min-h-[calc(100vh-80px)] relative bg-neutral-900 container flex flex-col items-center"
           id="experience">
    <h2 class="text-6xl font-bold text-center mb-6">Experience</h2>
    <article class="relative w-full pl-16">

      <div v-for="exp in experiences" :key="exp.title" class="relative pb-2 mb-1">
        <div class="absolute h-full flex flex-col items-center top-0.5 -left-12 ">
          <div class="h-6 w-6 rounded-full bg-emerald-300 "></div>
          <div class="h-[calc(100%-40px)] w-0.5 bg-purple-500 mt-auto"></div>
        </div>
        <h3 class="text-xl text-emerald-500 mb-2">{{ exp.year }}</h3>
        <p class="text-3xl text-purple-500 mb-2">{{ exp.title }}</p>
        <p class="text-neutral-400 mb-2">{{ exp.description }}</p>
        <ul class="flex gap-4">
          <li v-for="tech in exp.technologies" :key="tech"
              class="p-2 px-4 border rounded-2xl text-emerald-300 border-purple-300">{{
              tech
            }}
          </li>
        </ul>
      </div>

    </article>
  </section>


</template>

<style scoped>

</style>