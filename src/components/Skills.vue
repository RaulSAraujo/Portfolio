<template>
  <div>
    <v-toolbar
      color="grey-darken-4"
      width="100%"
      class="py-5 align-center justify-center"
    >
      <v-row no-gutters justify="center">
        <span class="text-h2"> HABILIDADES </span>
      </v-row>
    </v-toolbar>

    <v-card width="100%" height="400" class="pa-5" color="black">
      <v-row justify="center" class="mt-12">
        <v-sheet color="black" :width="!useDisplay.smAndDown ? '20%' : '50%'">
          <v-row no-gutters justify="space-evenly">
            <v-col
              v-for="skill in skills"
              :key="skill"
              cols="4"
              sm="4"
              md="4"
              lg="4"
              xl="4"
            >
              <v-hover>
                <template v-slot:default="{ isHovering, props }">
                  <v-icon
                    v-bind="props"
                    :icon="skill.icon"
                    size="60"
                    :color="isHovering ? skill.color : undefined"
                    @mouseenter="tab = skill.value"
                  ></v-icon>
                </template>
              </v-hover>
            </v-col>
          </v-row>
        </v-sheet>

        <v-sheet :width="!useDisplay.smAndDown ? '30%' : '100%'" color="black">
          <v-window v-model="tab">
            <v-window-item
              v-for="skill in skills"
              :key="skill"
              :value="skill.value"
            >
              <v-card flat color="black">
                <v-card-title class="text-h4">{{ skill.title }}</v-card-title>
                <v-card-subtitle class="mt-n2">{{
                  skill.subtitle
                }}</v-card-subtitle>
                <v-card-text class="text-body-1">
                  {{ skill.text }}
                </v-card-text>
              </v-card>
            </v-window-item>
          </v-window>
        </v-sheet>
      </v-row>
    </v-card>
  </div>
</template>

<script>
import { useDisplay } from "vuetify";
export default {
  data() {
    return {
      useDisplay: useDisplay(),
      tab: "HTML",
      skills: [
        {
          value: "HTML",
          title: "HTML",
          text: "É uma linguagem de marcação utilizada na construção de paginas Web",
          subtitle: "3 anos de experiência com esta tecnologia.",
          icon: "mdi-language-html5",
          color: "orange",
        },
        {
          value: "CSS",
          title: "CSS",
          text: "É um mecanismo para adicionar estilo a um documento Web",
          subtitle: "3 anos de experiência com esta tecnologia.",
          icon: "mdi-language-css3",
          color: "blue",
        },
        {
          value: "JAVA SCRIPT",
          title: "JAVA SCRIPT",
          text: "É uma linguagem de programação. Juntamente com HTML e CSS, é uma das três principais tecnologias da Web",
          subtitle: "2 anos de experiência com esta tecnologia.",
          icon: "mdi-language-javascript",
          color: "yellow",
        },
        {
          value: "GIT",
          title: "GIT",
          text: "É um sistema de controle de versões distribuido usado principalmente no desenvolvimento de software.",
          subtitle: "2 anos de experiência com esta tecnologia.",
          icon: "mdi-git",
          color: "red",
        },
        {
          value: "GITHUB",
          title: "GITHUB",
          text: "É uma plataforma de hospedagem de código-fonte e arquivos com controle de versão usando o Git.",
          subtitle: "2 anos de experiência com esta tecnologia.",
          icon: "mdi-git",
          color: "red",
        },
        {
          value: "VUE JS",
          title: "VUE JS",
          text: "É um framework JavaScript de código aberto para a criação de aplicações web",
          subtitle: "2 anos de experiência com esta tecnologia.",
          icon: "mdi-vuejs",
          color: "green",
        },
        {
          value: "VUETIFY",
          title: "VUETIFY",
          text: "É um frameworks CSS para o desenvolvimento de sites e sistemas de maneira mais rápida e otimizada.",
          subtitle: "Tenha 2 anos de experiência com esta tecnologia.",
          icon: "mdi-vuetify",
          color: "blue",
        },
      ],
    };
  },
  methods: {},
};
</script>

<style>
</style>