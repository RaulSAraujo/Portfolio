<template>
  <v-app>
    <v-main>
      <AppBar
        ref="AppBar"
        @scrollToStart="scrollToStart"
        @scrollToAboutMe="scrollToAboutMe"
        @scrollToProjects="scrollToProjects"
        @scrollToSkills="scrollToSkills"
      />
      <Home ref="Home" />
    </v-main>
  </v-app>
</template>

<script >
import Home from "@/views/LandingPage.vue";
import AppBar from "@/components/AppBar.vue";
export default {
  components: {
    Home,
    AppBar,
  },
  data() {
    return {};
  },
  methods: {
    scrollToStart() {
      this.$refs.Home.scrollById("start");
    },
    scrollToAboutMe() {
      this.$refs.Home.scrollById("aboutMe");
    },
    scrollToProjects() {
      this.$refs.Home.scrollById("projects");
    },
    scrollToSkills() {
      this.$refs.Home.scrollById("skills");
    },
  },
};
</script>
