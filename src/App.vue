<script setup>
import navbar from "./components/navbar.vue";
import homeAboutMeVue from "./sections/home-about-me.vue";
import homeExperienceVue from "./sections/home-experience.vue";
import homeHeroVue from "./sections/home-hero.vue";
import homeProjects from "./sections/home-projects.vue";
import myFooter from "./components/my-footer.vue";
</script>
<template>
  <navbar />
  <homeHeroVue />
  <homeAboutMeVue />
  <homeExperienceVue />
  <home-projects />
  <myFooter />
</template>
