<script setup lang="ts">
import NavBar from "@/components/NavBar.vue";
import Home from "@/components/Home.vue";
import About from "@/components/About.vue";
import Skills from "@/components/Skills.vue";
import Projects from "@/components/Projects.vue";
import Experience from "@/components/Experience.vue";
import Setup from "@/components/Setup.vue";
import Contact from "@/components/Contact.vue";
</script>

<template>
  <main class="w-full relative">
    <NavBar/>
    <Home/>
    <About/>
    <Skills/>
    <Projects/>
    <Experience/>
    <Setup/>
    <Contact/>
  </main>
</template>

<style scoped>
</style>
