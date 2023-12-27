<script setup lang="ts">

const scrollToSection = (section: string) => {
  const el = document.getElementById(section);
  const navbarHeight = 80;
  if (el) {
    const offsetTop = el.offsetTop - navbarHeight;
    window.scrollTo({top: offsetTop, behavior: "smooth"});
  }
}
</script>

<template>
  <header
      class="flex w-full h-20 px-28 items-center justify-center sticky backdrop-blur-sm bg-neutral-700/95 top-0 z-10">
    <div class="absolute top-0 bottom-0 left-20">
      <div class="flex h-full items-center text-4xl font-bold">
        <span class="text-emerald-500">Alex</span>
        <span>.</span>
        <span class="text-purple-500">dev</span>
      </div>
    </div>
    <nav>
      <ul class="flex text-xl gap-7 lowercase text-neutral-400">
        <li class=" hover:text-neutral-50">
          <a @click="scrollToSection('home')">Home</a>
        </li>
        <li class=" hover:text-neutral-50">
          <a @click="scrollToSection('about')">About</a>
        </li>
        <li class=" hover:text-neutral-50">
          <a @click="scrollToSection('skills')">Skills</a>
        </li>
        <li class=" hover:text-neutral-50">
          <a @click="scrollToSection('projects')">Projects</a>
        </li>
        <li class=" hover:text-neutral-50">
          <a @click="scrollToSection('experience')">Experience</a>
        </li>
        <li class=" hover:text-neutral-50">
          <a @click="scrollToSection('setup')">Setup</a>
        </li>
        <li class=" hover:text-neutral-50">
          <a @click="scrollToSection('contact')">Contact</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>

</style>