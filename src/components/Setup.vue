<script setup lang="ts">

import {ref} from "vue";

const setupImgs = ref(
    [
      {src: "../assets/setup4.jpg", alt: "setup"},
      {src: "../assets/setup3.jpg", alt: "setup"},
      {src: "../assets/setup2.jpg", alt: "setup"},
      {src: "../assets/setup1.jpg", alt: "setup"},
    ]
);

const getImageUrl = (path: string) => {
  return new URL(`${path}`, import.meta.url).href;
};

</script>

<template>
  <section class="min-h-[calc(100vh-80px)] relative bg-neutral-900 container flex flex-col items-center" id="setup">
    <h2 class="text-6xl font-bold text-center mb-6">My Setup</h2>
    <article class="w-9/12 grid grid-cols-5 grid-rows-2 rounded-lg overflow-hidden shadow-lg shadow-purple-500">
      <img :src="getImageUrl(setupImgs[0].src)" :alt="setupImgs[0].alt"
           class="w-full h-full object-cover row-span-2 col-span-3"/>
      <img :src="getImageUrl(setupImgs[1].src)" :alt="setupImgs[1].alt"
           class="w-full h-auto object-cover row-span-1 col-span-2"/>
      <img :src="getImageUrl(setupImgs[3].src)" :alt="setupImgs[3].alt"
           class="w-full h-auto object-cover row-span-1 col-span-2"/>
    </article>
  </section>

</template>

<style scoped>

</style>