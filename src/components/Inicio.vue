<template>
  <v-app class="align-center">
    <v-card
      :class="!useDisplay.xs ? 'ma-7 pa-4' : ''"
      rounded="xl"
      color="rgb(0,0,0,0)"
      elevation="0"
    >
      <v-row no-gutters align="center">
        <v-col cols="12" sm="12" md="5" lg="6" xl="6">
          <Vue3Lottie
            animationLink="https://assets2.lottiefiles.com/packages/lf20_w51pcehl.json"
          />
        </v-col>
        <v-col cols="12" sm="12" md="7" lg="6" xl="6">
          <v-card color="rgb(0,0,0,0)" elevation="0">
            <v-card-title>
              <span class="text-h6">Oi, eu sou</span>
              <v-row
                class="text-h4 text-sm-h2 text-md-h2 text-lg-h2"
                no-gutters
              >
                <p v-html="animatedName"></p>
                <span :class="{ show: iconVisible, hide: !iconVisible }"
                  >|</span
                >
              </v-row>
            </v-card-title>

            <v-card-subtitle class="mt-n2"
              >Desenvolvedor Front-end</v-card-subtitle
            >

            <v-card-actions>
              <v-btn
                prepend-icon="mdi-linkedin"
                variant="plain"
                size="large"
                height="https://www.linkedin.com/in/raulsaraujo/"
                target="_blank"
                >Linkedin</v-btn
              >
              <v-btn
                prepend-icon="mdi-github"
                variant="plain"
                size="large"
                href="https://github.com/RaulSAraujo"
                target="_blank"
                >GitHub</v-btn
              >
              <v-btn
                prepend-icon="mdi-gitlab"
                variant="plain"
                size="large"
                href="https://gitlab.com/Raul.sAraujo"
                target="_blank"
                >GitLab</v-btn
              >
            </v-card-actions>
          </v-card>
          <v-row no-gutters class="px-4">
            <span>Seja muito bem vindo ao meu portfólio.</span>
          </v-row>
        </v-col>
      </v-row>
    </v-card>
    <v-row class="mb-15" no-gutters align="end" justify="center">
      <Vue3Lottie
        animationLink="https://assets2.lottiefiles.com/packages/lf20_x1kgpavt.json"
        :height="80"
        :width="80"
      />
    </v-row>
  </v-app>
</template>

<script>
import { Vue3Lottie } from "vue3-lottie";
import { useDisplay } from "vuetify";
export default {
  components: {
    Vue3Lottie,
  },
  mounted() {
    this.animateName();
    setInterval(() => {
      this.iconVisible = !this.iconVisible;
    }, 1000);
  },
  data() {
    return {
      useDisplay: useDisplay(),
      name: "Raul Silva Araujo",
      animatedName: "",
      iconVisible: true,
    };
  },
  methods: {
    animateName() {
      let i = 0;
      const idIntervalo = setInterval(() => {
        if (i < this.name.length) {
          this.animatedName += this.name.charAt(i);
          i++;
        } else {
          clearInterval(idIntervalo);
        }
      }, 60);
    },
  },
};
</script>

<style>
.show {
  opacity: 1;
  transition: opacity 0.1s ease-in-out;
}
.hide {
  opacity: 0;
  transition: opacity 0.1s ease-in-out;
}
</style>