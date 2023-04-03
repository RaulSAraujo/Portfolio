<template>
  <Inicio id="start" />
  <AboutMe id="aboutMe" />
  <Projects id="projects" />
  <Skiils id="skills" />
</template>

<script>
import { Vue3Lottie } from "vue3-lottie";

import Inicio from "@/components/Inicio.vue";
import AboutMe from "@/components/AboutMe.vue";
import Projects from "@/components/Projects.vue";
import Skiils from "@/components/Skills.vue"
export default {
  components: {
    Vue3Lottie,
    Inicio,
    AboutMe,
    Projects,
    Skiils,
  },
  data() {
    return {};
  },

  methods: {
    scrollById(id) {
      const el = document.getElementById(id);
      const elCoordenadas = el.getBoundingClientRect();
      window.scrollBy(elCoordenadas.x, elCoordenadas.y);
    },
  },
};
</script>

<style>
</style>
