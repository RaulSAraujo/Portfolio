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
import Skiils from "@/components/Skills.vue";
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
      setTimeout(() => {
        var elemento = document.getElementById(id);
        if (id == "projects") {
          this.animarScroll(elemento.offsetTop - 60, 1000);
        } else if (id == "skills") {
          this.animarScroll(elemento.offsetTop - 60, 1000);
        } else {
          this.animarScroll(elemento.offsetTop, 1000);
        }
      }, 50);
    },
    animarScroll(destino, duracao) {
      var inicio = window.pageYOffset;
      var distancia = destino - inicio;
      var duracaoAtual = 0;
      var passo = 20;

      requestAnimationFrame(animacaoScroll);

      function animacaoScroll() {
        duracaoAtual += passo;

        var posicao = inicio + distancia * (duracaoAtual / duracao);

        window.scrollTo(0, posicao);

        if (duracaoAtual < duracao) {
          requestAnimationFrame(animacaoScroll);
        }
      }
    },
  },
};
</script>

<style>
</style>
