<template>
  <v-app-bar>
    <v-app-bar-title>
      <v-row no-gutters align="center">
        <span class="ml-2 text-subtitle-1" v-text="'<'"></span>
        <span class="text-h5 mx-1" v-text="'RA'"></span>
        <span class="text-subtitle-1" v-text="'/>'"></span>

        <v-spacer v-if="!useDisplay.xs"></v-spacer>
        <v-btn-group v-if="!useDisplay.xs">
          <v-btn variant="plain" @click="scrollToStart">Inicio</v-btn>
          <v-btn variant="plain" @click="scrollToAboutMe">Sobre mim</v-btn>
          <v-btn variant="plain" @click="scrollToProjects">Projetos</v-btn>
          <v-btn variant="plain" @click="scrollToSkills">Habilidades</v-btn>
        </v-btn-group>
        <v-spacer></v-spacer>

        <v-menu v-if="useDisplay.xs" location="start">
          <template v-slot:activator="{ props }">
            <v-btn class="mr-2" icon="mdi-menu" v-bind="props"></v-btn>
          </template>

          <v-list>
            <v-list-item @click="scrollToStart">
              <v-list-item-title>Inicio</v-list-item-title>
            </v-list-item>
            <v-list-item  @click="scrollToAboutMe">
              <v-list-item-title>Sobre mim</v-list-item-title>
            </v-list-item>
            <v-list-item @click="scrollToProjects">
              <v-list-item-title>Projetos</v-list-item-title>
            </v-list-item>
            <v-list-item @click="scrollToSkills">
              <v-list-item-title>Habilidades</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </v-row>
    </v-app-bar-title>
  </v-app-bar>
</template>

<script>
import { useDisplay } from "vuetify";
export default {
  data() {
    return {
      useDisplay: useDisplay(),
    };
  },
  methods: {
    scrollToStart() {
      this.$emit("scrollToStart");
    },
    scrollToAboutMe() {
      this.$emit("scrollToAboutMe");
    },
    scrollToProjects() {
      this.$emit("scrollToProjects");
    },
    scrollToSkills() {
      this.$emit("scrollToSkills");
    },
  },
};
</script>

<style>
</style>