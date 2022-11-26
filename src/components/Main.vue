<template>
  <main
    id="project"
    class="flex flex-wrap gap-6 justify-center 2xl:grid 2xl:grid-cols-4 2xl:gap-10 2xl:justify-start mt-10 2xl:w-[1200px] 2xl:mx-auto"
  >
    <Card :project-data="projectData" />
    <div
      @click="backToTop"
      class="fixed cursor-pointer right-2"
      v-show="scrollY > 300"
    >
      <svg
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M17.6568 8.96219L16.2393 10.3731L12.9843 7.10285L12.9706 20.7079L10.9706 20.7059L10.9843 7.13806L7.75404 10.3532L6.34314 8.93572L12.0132 3.29211L17.6568 8.96219Z"
          fill="currentColor"
        />
      </svg>
    </div>
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
import { onMounted } from "vue";
import { ref } from "vue";
import Card from "./Card.vue";
import projectData from "../data/project";

const scrollTimer = ref(0);
const scrollY = ref(0);

const handleScroll = () => {
  if (scrollTimer.value) return;

  scrollTimer.value = setTimeout(() => {
    scrollY.value = window.scrollY;
    clearTimeout(scrollTimer.value);
    scrollTimer.value = 0;
  }, 100);
};

const backToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: "smooth",
  });
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});
</script>
