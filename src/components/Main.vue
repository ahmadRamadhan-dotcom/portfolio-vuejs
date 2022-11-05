<template>
  <main
    id="project"
    class="flex flex-wrap gap-6 justify-center 2xl:grid 2xl:grid-cols-4 2xl:gap-10 2xl:justify-start mt-10 2xl:w-[1200px] 2xl:mx-auto"
  >
    <Card :project-data="projectData" />
  </main>
  <h2 class="text-center text-white mt-10 text-lg">
    More project on
    <a
      href="https://github.com/ahmadRamadhan-dotcom"
      target="_blank"
      class="underline"
      >github</a
    >
  </h2>
</template>

<script setup>
import Card from "./Card.vue";
import projectData from "../data/project";
</script>
