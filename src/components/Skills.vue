<template>
  <div>
    <v-toolbar color="background" width="100%" class="py-5 align-center justify-center" border="md">
      <v-row no-gutters justify="center">
        <span class="text-h2"> HABILIDADES </span>
      </v-row>
    </v-toolbar>

    <v-card width="100%" height="400" class="pa-4" color="black">
      <v-row justify="center" class="mt-12">
        <v-sheet color="black" :width="!useDisplay.smAndDown ? '300' : '200'">
          <v-row no-gutters justify="space-evenly">
            <v-col v-for="skill in skills" :key="skill" cols="4" sm="4" md="4" lg="4" xl="4">
              <v-hover>
                <template v-slot:default="{ isHovering, props }">
                  <v-icon v-if="skill.icon != null" v-bind="props" :icon="skill.icon" size="60"
                    :color="isHovering ? skill.color : undefined" @mouseenter="tab = skill.value">
                  </v-icon>

                  <IconBase v-else-if="skill.title == 'FLUTTER'" class="mt-n1" v-bind="props" iconName="Flutter"
                    :width="40" :height="60" :color="isHovering ? skill.color : undefined" @mouseenter="tab = skill.value">
                    <IconFlutter />
                  </IconBase>
                </template>
              </v-hover>
            </v-col>
          </v-row>
        </v-sheet>

        <v-sheet v-if="tab == undefined" :width="!useDisplay.smAndDown ? '30%' : '100%'" color="black">
          <v-card flat color="black">
            <v-card-text class="text-body-1 text-center">
              {{
                !useDisplay.xs
                ? "Passe o mouse por cima para saber mais sobre minhas habilidades."
                : "Selecione um icone para saber mais sobre minhas habilidades."
              }}
            </v-card-text>
          </v-card>
        </v-sheet>

        <v-sheet v-else :width="!useDisplay.smAndDown ? '30%' : '100%'" color="black">
          <v-window v-model="tab">
            <v-window-item v-for="skill in skills" :key="skill" :value="skill.value">
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
import IconBase from "@/assets/svg/IconBase.vue";
import IconFlutter from "@/assets/svg/IconFlutter.vue";
export default {
  components: {
    IconBase,
    IconFlutter,
  },
  data() {
    return {
      useDisplay: useDisplay(),
      tab: undefined,
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
          icon: "mdi-github",
          color: "grey",
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
          color: "light-blue",
        },
        {
          value: "FLUTTER",
          title: "FLUTTER",
          text: "Flutter é um framework de desenvolvimento com foco multiplataforma em dispositivos móveis.",
          subtitle: "Tenha 2 anos de experiência com esta tecnologia.",
          icon: null,
          color: "blue",
        },
      ],
    };
  },
  methods: {},
};
</script>

<style></style>