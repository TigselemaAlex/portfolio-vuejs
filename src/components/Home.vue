<script setup lang="ts">


</script>

<template>
  <section class="w-full min-h-[calc(100vh-80px)]  h-[calc(100vh-80px)] relative" id="home">
    <div class="flex flex-col gap-4 justify-center items-center h-full hero bg-cover bg-center bg-no-repeat "
    >
      <h1 class="text-9xl font-bold font-sans  stroke-cyan-500 tracking-wide ">
        Alex Tigselema
      </h1>
      <h3 class="text-4xl font-bold font-sans tracking-widest">
        Software Engineer, Full Stack Developer
      </h3>
    </div>
    <div class="scroll-down"></div>
  </section>
</template>

<style scoped>
.hero {
  background-image: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.8)), url('@/assets/hero.jpg');
}

h1 {
  -webkit-text-stroke: 3px #10b981; /* width and color */
}

h3 {
  -webkit-text-stroke: 1px #9333ea; /* width and color */
}

.scroll-down {
  position: absolute;
  left: 50%;
  bottom: 50px;
  display: block;
  text-align: center;
  font-size: 30px;
  text-decoration: none;
  width: 23px;
  height: 23px;
  border-bottom: 4px solid #fff;
  border-right: 4px solid #fff;
  z-index: 9;
  -webkit-transform: translate(-50%, 0%) rotate(45deg);
  -moz-transform: translate(-50%, 0%) rotate(45deg);
  transform: translate(-50%, 0%) rotate(45deg);
  -webkit-animation: fade_move_down 2s ease-in-out infinite;
  -moz-animation: fade_move_down 2s ease-in-out infinite;
  animation: fade_move_down 2s ease-in-out infinite;
}

@-webkit-keyframes fade_move_down {
  0% {
    -webkit-transform: translate(0, -10px) rotate(45deg);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    -webkit-transform: translate(0, 10px) rotate(45deg);
    opacity: 0;
  }
}

@-moz-keyframes fade_move_down {
  0% {
    -moz-transform: translate(0, -10px) rotate(45deg);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    -moz-transform: translate(0, 10px) rotate(45deg);
    opacity: 0;
  }
}

@keyframes fade_move_down {
  0% {
    transform: translate(0, -10px) rotate(45deg);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    transform: translate(0, 10px) rotate(45deg);
    opacity: 0;
  }
}

</style>