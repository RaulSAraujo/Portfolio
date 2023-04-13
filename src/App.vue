<template>
  <v-app>
    <AppBar
      ref="AppBar"
      @scrollToStart="scrollToStart"
      @scrollToAboutMe="scrollToAboutMe"
      @scrollToProjects="scrollToProjects"
      @scrollToSkills="scrollToSkills"
    />
    <v-main>
      <LandingPage ref="LandingPage" />
    </v-main>
  </v-app>
</template>

<script >
import LandingPage from "@/views/LandingPage.vue";
import AppBar from "@/components/AppBar.vue";
export default {
  components: {
    LandingPage,
    AppBar,
  },
  data() {
    return {};
  },
  methods: {
    scrollToStart() {
      this.$refs.LandingPage.scrollById("start");
    },
    scrollToAboutMe() {
      this.$refs.LandingPage.scrollById("aboutMe");
    },
    scrollToProjects() {
      this.$refs.LandingPage.scrollById("projects");
    },
    scrollToSkills() {
      this.$refs.LandingPage.scrollById("skills");
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html * {
  font-family: "Yantramanav", sans-serif !important;
}

::-webkit-scrollbar {
  width: 10px;
  background-color: rgb(1, 1, 1);
  border-radius: 5px;
}
</style>
