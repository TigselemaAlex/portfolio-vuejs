<script setup lang="ts">

</script>

<template>
  <section class="h-[calc(100vh-80px)] relative bg-neutral-900 container" id="about">
    <h2 class="text-6xl font-bold text-center mb-6">About Me</h2>
    <article class="flex gap-10">
      <div class="w-full flex flex-col">
        <h3 class="text-2xl mb-4 text-neutral-400">Hi there!!!</h3>
        <p class="text-4xl text-neutral-200">I'm Alex, a full stack developer specializing in Angular and Spring Boot.
          Proficient in crafting dynamic interfaces and robust backend systems, I create seamless, scalable applications
          for several needs.</p>
        <div class="flex gap-4 mt-auto text-4xl px-6">
          <a href="https://github.com/TigselemaAlex" target="_blank"
             class="p-2 border-2 rounded-full flex items-center border-neutral-300 text-neutral-300 hover:-translate-y-0.5 transition-all hover:text-neutral-50 hover:border-neutral-50">
            <i class='bx bxl-github'></i>
          </a>
          <a href="https://www.linkedin.com/in/alex-tigselema-pacheco-a66b92227/" target="_blank"
             class="p-2 border-2 rounded-full flex items-center border-indigo-500 text-indigo-500 hover:-translate-y-0.5 transition-all
                hover:text-indigo-400 hover:border-indigo-400">
            <i class='bx bxl-linkedin-square'></i>
          </a>
        </div>
      </div>
      <div class="profile"></div>
    </article>
  </section>
</template>

<style scoped>
.profile {
  min-width: 400px;
  min-height: 400px;
  background-image: url('src/assets/profile.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  border-radius: 50%;
}
</style>