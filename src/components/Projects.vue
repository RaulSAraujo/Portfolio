<template>
  <v-app>
    <v-toolbar
      color="background"
      width="100%"
      class="py-5 align-center justify-center"
      border="md"
    >
      <v-row no-gutters justify="center">
        <span class="text-h2"> PROJETOS </span>
      </v-row>
    </v-toolbar>

    <v-row justify="center" align="center">
      <v-sheet
        width="100%"
        color="rgb(26, 25, 25)"
        :height="!useDisplay.smAndDown ? '500' : ''"
        class="d-flex align-center"
      >
        <v-row dense class="pa-2 mx-5" align="center">
          <v-col
            v-for="project in projects"
            :key="project"
            cols="12"
            sm="12"
            md="6"
            lg="4"
            xl="4"
          >
            <v-card
              color="rgb(0,0,0)"
              width="100%"
              height="300"
              rounded="xl"
              elevation="0"
              border="md"
            >
              <v-img
                v-if="project.name != 'Em breve'"
                :src="project.image"
                height="150"
                cover
              >
                <v-sheet
                  height="100%"
                  color="rgb(0,0,0,0.5)"
                  class="d-flex align-end"
                >
                  <v-card color="rgb(0,0,0,0.0)">
                    <v-card-title class="text-h4">{{
                      project.name
                    }}</v-card-title>
                    <v-card-subtitle>
                      <v-row no-gutters>
                        <div v-for="sub in project.sub" :key="sub">
                          <v-icon
                            class="mx-1"
                            :icon="sub.icon"
                            :color="sub.color"
                          ></v-icon>
                          <span>{{ sub.text }}</span>
                        </div>
                      </v-row>
                    </v-card-subtitle>
                  </v-card>
                </v-sheet>
              </v-img>

              <v-card-text
                v-if="project.name != 'Em breve'"
                class="text-body-1"
              >
                <p
                  style="
                    display: -webkit-box;
                    max-width: 1000;
                    -webkit-box-orient: vertical;
                    -webkit-line-clamp: 3;
                    overflow: hidden;
                  "
                  class="text-body-2"
                >
                  {{ project.text }}
                </p>
              </v-card-text>
              <v-card-actions v-if="project.name != 'Em breve'" class="mr-2">
                <v-spacer></v-spacer>

                <v-btn
                  :href="project.url"
                  target="_blank"
                  prepend-icon="mdi-link"
                  variant="outlined"
                  color="blue"
                  rounded="lg"
                  >Visualizar</v-btn
                >
              </v-card-actions>

              <v-card
                v-if="project.name == 'Em breve'"
                color="white"
                style="opacity: 0.7"
              >
                <v-img
                  src="@/assets/img/EmBreve.jpeg"
                  height="300"
                  style="transform: rotate(28deg)"
                ></v-img>
              </v-card>
            </v-card>
          </v-col>
        </v-row>
      </v-sheet>
    </v-row>
  </v-app>
</template>

<script>
import { useDisplay } from "vuetify";
export default {
  data() {
    return {
      useDisplay: useDisplay(),
      projects: [
        {
          name: "Multi Plus Streaming",
          sub: [
            { text: "Vue.Js", icon: "mdi-vuejs", color: "green" },
            { text: "Vuetify", icon: "mdi-vuetify", color: "blue" },
          ],
          text: "Site de filmes, series e livros que permita aos usuários realizarem um cadastro, adicionar suas obras favoritas em uma lista personalizada, consultar informações, marcar os assistidos/lidos e verificar em qual plataforma o mesmo estará disponivel.",
          url: "https://multi-plus-streaming.vercel.app/",
          image:
            "https://front-3t5xttaqp-raulsaraujo.vercel.app/assets/Backgroud.6f70cb0d.png",
        },
        {
          name: "Make a List",
          sub: [
            { text: "React.js", icon: "mdi-react", color: "blue" },
            { text: "Chakra.ui", icon: "mdi-lightning-bolt", color: "cyan" },
            { text: "Typescript", icon: "mdi-language-typescript", color: "blue" },
          ],
          text: "Crie listas de compras detalhadas, incluindo produtos, preços e locais de compra.",
          url: "https://make-a-list.vercel.app/",
          image:
            "https://raw.githubusercontent.com/jpfalcuci/dsm3-projeto_integrador-make_a_list/main/.github/Web.png",
        },
        {
          name: "Em breve",
        },
      ],
    };
  },
  methods: {},
};
</script>

<style>
</style>
