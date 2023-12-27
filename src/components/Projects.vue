<script setup lang="ts">

import {ref} from "vue";
import 'vue3-carousel/dist/carousel.css'
import {Carousel, Navigation, Pagination, Slide} from 'vue3-carousel'

const projects = ref([
  {
    name: "One Alarm",
    description: "This project is a Panic Button System designed to provide a safety mechanism for stores. The system consists of a desktop client developed with Electron and React, a mobile client, and a backend REST API developed with Spring Boot. The system allows an admin user to add stores, locate them on a Google Maps component, and assign a user to each store. The store owners can then log in using the assigned user credentials and trigger a panic alert to notify all other users, including the admin, through push notifications.",
    participation: "I developed all the backend of the application using the Spring Boot framework. For this I used Spring Framework projects: Spring JPA and Lombok.",
    technologies: [
      "Java",
      "Spring Boot",
      "MySQL",
      "React",
      "Electron",
      "Google Maps API",
      "Firebase Cloud Messaging"
    ],
    images: [
      {src: "../assets/panic-button.png"}
    ],
    githubLinks: [
      {
        link: "https://github.com/noesrichard/proyecto-distribuidas"
      }
    ]
  },
  {
    name: "HOTELCLOUD",
    description: "This project is a web management system for hotel reservations where you can manage customers, manage rooms and manage reservation. The client side project is developed with Angular v13 and with the PrimeNg UI components library together with the PrimeFlex library. The backend part is completely developed in the Spring Boot 2.7.5 framework with the Spring Framework modules: Spring JPA and Lombok. As for the database, MySql was used.",
    participation: "I developed the entire project.",
    technologies: [
      "Java",
      "Spring Boot",
      "MySQL",
      "Angular",
      "PrimeNg",
      "PrimeFlex",
    ],
    images: [
      {src: "../assets/hotelcloud1.png"},
      {src: "../assets/hotelcloud2.png"},
      {src: "../assets/hotelcloud3.png"},
      {src: "../assets/hotelcloud4.png"},
      {src: "../assets/hotelcloud5.png"},
      {src: "../assets/hotelcloud6.png"},
      {src: "../assets/hotelcloud7.png"},
    ],
    githubLinks: [
      {
        link: "https://github.com/TigselemaAlex/GestionHoteleraBackend"
      }, {
        link: "https://github.com/TigselemaAlex/gestionProyecto"
      }
    ]
  },
  {
    name: "Bus-Link",
    description: "It is a multiplatform system for the administration and purchase of travel tickets for bus land terminals. In this system as administrator we can manage the cooperatives and their buses, the users of the system, and assign the frequencies to be used by the registered cooperatives. As administrator users of each cooperative we will be able to make ticket sales. As a customer I can make reservations in the web application or the mobile application.",
    participation: "I developed the API that both the web and mobile applications use. For this I used Spring Framework projects: Spring JPA, Lombok, Spring Security and JWT",
    technologies: [
      "Java",
      "Spring Boot",
      "MongoDB",
      "React",
      "Flutter"
    ],
    images: [
      {
        src: "../assets/buslink1.png"
      },
      {
        src: "../assets/buslink2.png"
      },
      {
        src: "../assets/buslink3.png"
      },
      {
        src: "../assets/buslink4.png"
      },
      {
        src: "../assets/buslink5.png"
      },
      {
        src: "../assets/buslink6.png"
      },
      {
        src: "../assets/buslink7.png"
      },
      {
        src: "../assets/buslink8.png"
      },
      {
        src: "../assets/buslink9.png"
      },
      {
        src: "../assets/buslink10.png"
      },
      {
        src: "../assets/buslink11.png"
      },
      {
        src: "../assets/buslink12.png"
      },
      {
        src: "../assets/buslink13.jpg"
      },
      {
        src: "../assets/buslink14.jpg"
      },
      {
        src: "../assets/buslink15.png"
      },
      {
        src: "../assets/buslink16.jpg"
      },
      {
        src: "../assets/buslink17.png"
      },
      {
        src: "../assets/buslink18.jpg"
      },
      {
        src: "../assets/buslink19.jpg"
      },
    ],
    githubLinks: [
      {
        link: "https://github.com/TigselemaAlex/buslink-backend"
      }
    ]

  }

]);

const getImageUrl = (path: string) => {
  return new URL(`${path}`, import.meta.url).href;
};
</script>

<template>

  <section class="min-h-[calc(100vh-80px)] relative bg-neutral-900 container flex flex-col items-center" id="projects">
    <h2 class="text-6xl font-bold text-center mb-6">Projects</h2>
    <div v-for="proyect in projects" :key="proyect.name"
         class="flex gap-4 w-full bg-neutral-700 p-4 border mb-8 rounded-lg">
      <div class="w-3/5">
        <h3 class="text-2xl text-purple-500 font-bold">{{ proyect.name }}</h3>
        <p class="text-emerald-500 my-2">Description:</p>
        <p class="text-sm text-neutral-300">{{ proyect.description }}</p>
        <p class="text-emerald-500 my-2">Participation:</p>
        <p class="text-sm ">{{ proyect.participation }}</p>
        <p class="text-emerald-500 my-2">Technologies:</p>
        <ul class="flex gap-2">
          <li v-for="technology in proyect.technologies" :key="technology"
              class="text-xs rounded-xl border p-1 px-2 text-amber-100 border-amber-100">{{
              technology
            }}
          </li>
        </ul>
      </div>
      <div class="w-2/5 flex flex-col gap-4 ">

        <carousel :autoplay="2000" :wrap-around="true" class="bg-neutral-500 py-2 rounded">
          <slide v-for="image of proyect.images" :key="proyect.name">
            <img :src="getImageUrl(image.src)" alt="image" class="max-h-80 ">
          </slide>
          <template #addons>
            <navigation/>
            <pagination/>
          </template>
        </carousel>

        <div>
          <p class="text-emerald-500 mb-2">GitHub:</p>
          <ul class="flex gap-2 flex-col">
            <li v-for="link in proyect.githubLinks" :key="link.link">
              <a :href="link.link" target="_blank"
                 class="text-xs rounded-xl border p-1 px-2 text-amber-100 border-amber-100">
                {{ link.link }}
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>

</template>

<style scoped>

</style>