<script setup lang="ts">

</script>

<template>

  <section class="min-h-[calc(100vh-80px)] relative bg-neutral-900 container flex flex-col items-center" id="contact">
    <h2 class="text-6xl font-bold text-center mb-6">Contact</h2>

    <div class="w-[720px]">
      <h3 class="text-3xl text-purple-500 font-bold">Get in touch</h3>
      <p class="text-neutral-300">Ready to collaborate? Drop me a message outlining how I can assist you. Let's team up
        and make your software
        goals a reality. Get in touch, and let's build something incredible together.</p>
      <form class="grid grid-rows-4 grid-cols-2 gap-x-2 mt-4">
        <div class="row-span-1 col-span-1">
          <label for="name" class="text-emerald-500">Name</label>
          <input type="text" id="name" name="name" placeholder="Your name"
                 class="w-full p-2 rounded-lg border bg-neutral-700 placeholder-neutral-400"/>
        </div>
        <div class="row-span-1 col-span-1">
          <label for="email" class="text-emerald-500">Email</label>
          <input type="email" id="email" name="email" placeholder="Your email"
                 class="w-full p-2 rounded-lg border bg-neutral-700 placeholder-neutral-400"/>
        </div>
        <div class="row-span-2 col-span-2">
          <label for="message" class="text-emerald-500">Message</label>
          <textarea id="message" name="message" placeholder="Your message"
                    class="w-full p-2 rounded-lg border h-32 bg-neutral-700 placeholder-neutral-400"></textarea>
        </div>
        <div class="row-span-1 col-span-2 mt-2">
          <button type="button"
                  class="w-full bg-emerald-500 text-white p-2 rounded-lg font-bold text-2xl uppercase hover:bg-emerald-600">
            Send
          </button>
        </div>
      </form>
    </div>
  </section>
</template>

<style scoped>

</style>