<template>
  <main
    id="project"
    class="flex flex-wrap gap-6 justify-center 2xl:grid 2xl:grid-cols-4 2xl:gap-10 2xl:justify-start mt-10 2xl:w-[1200px] 2xl:mx-auto"
  >
    <Card :project-data="projectData" />
  </main>
</template>

<script setup>
import Card from "./Card.vue";
import projectData from "../data/project";
</script>
