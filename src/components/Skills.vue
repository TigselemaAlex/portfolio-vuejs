<script setup lang="ts">
import {ref} from "vue";

enum SkillLevel {
  BEGINNER = "beginner",
  INTERMEDIATE = "intermediate",
  ADVANCED = "advanced"
}

const skills = ref([
  {
    name: "Angular",
    icon: "bx bxl-angular",
    color: "text-red-500",
    level: SkillLevel.ADVANCED
  },
  {name: "Vue", icon: "bx bxl-vuejs", color: "text-green-600", level: SkillLevel.BEGINNER},
  {name: "Spring Boot", icon: "bx bxl-spring-boot", color: "text-green-500", level: SkillLevel.ADVANCED},
  {name: "MongoDB", icon: "bx bxl-mongodb", color: "text-emerald-600", level: SkillLevel.INTERMEDIATE},
  {name: "Laravel", icon: "bx bxl-php", color: "text-blue-500", level: SkillLevel.INTERMEDIATE},
  {name: "Electronjs", icon: "bx bxl-nodejs", color: "text-cyan-500", level: SkillLevel.INTERMEDIATE},
  {name: "PostgreSQL", icon: "bx bxl-postgresql", color: "text-blue-400", level: SkillLevel.INTERMEDIATE},
  {name: "MySQL", icon: "bx bxs-data", color: "text-blue-600", level: SkillLevel.INTERMEDIATE},
  {name: "Docker", icon: "bx bxl-docker", color: "text-cyan-600", level: SkillLevel.BEGINNER},
  {name: "Git", icon: "bx bxl-git", color: "text-neutral-400", level: SkillLevel.INTERMEDIATE},
  {name: "Jira", icon: "bx bxs-spa", color: "text-blue-400", level: SkillLevel.BEGINNER},
  {name: "Java", icon: "bx bxl-java", color: "text-red-400", level: SkillLevel.ADVANCED},
  {name: "Go", icon: "bx bxl-nodejs", color: "text-cyan-500", level: SkillLevel.BEGINNER},
  {name: "HTML", icon: "bx bxl-html5", color: "text-orange-500", level: SkillLevel.INTERMEDIATE},
  {name: "CSS", icon: "bx bxl-css3", color: "text-blue-500", level: SkillLevel.INTERMEDIATE},
  {name: "SASS", icon: "bx bxl-sass", color: "text-pink-500", level: SkillLevel.INTERMEDIATE},
  {name: "Tailwind", icon: "bx bxl-tailwind-css", color: "text-cyan-500", level: SkillLevel.INTERMEDIATE},
  {name: "JavaScript", icon: "bx bxl-javascript", color: "text-yellow-500", level: SkillLevel.INTERMEDIATE},
  {name: "TypeScript", icon: "bx bxl-typescript", color: "text-indigo-500", level: SkillLevel.INTERMEDIATE},
  {name: "Python", icon: "bx bxl-python", color: "text-yellow-600", level: SkillLevel.BEGINNER},
  {name: "PHP", icon: "bx bxl-php", color: "text-cyan-500", level: SkillLevel.INTERMEDIATE},

]);

const getClassForSkill = (level: SkillLevel) => {
  const color = level === SkillLevel.ADVANCED ? "green-500" : level === SkillLevel.INTERMEDIATE ? "yellow-500" : "blue-500";
  return `text-${color}`;
}

</script>

<template>
  <section class="min-h-[calc(100vh-80px)] relative bg-neutral-900 container flex flex-col items-center" id="skills">
    <h2 class="text-6xl font-bold text-center mb-6">Skills</h2>
    <article
        class="grid grid-cols-5 justify-items-start w-full gap-2 rounded-lg">
      <div v-for="skill of skills"
           class="text-2xl flex flex-col border-2 w-full p-2 rounded-lg border-neutral-500 ">
        <div class="flex items-center gap-2 " :class="skill.color">
          <span :class="skill.color">{{ skill.name }}</span>
          <i :class="skill.icon" class="text-3xl"></i>
        </div>
        <div class="text-sm pl-6">
          <span>Level-> </span>
          <span :class="getClassForSkill(skill.level)">{{ skill.level }}</span>
        </div>
      </div>
    </article>
  </section>

</template>

<style scoped>

</style>