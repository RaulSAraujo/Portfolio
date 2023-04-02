<template>
  <v-responsive id="start" height="85vh" class="align-center">
    <v-card
      :class="!useDisplay.xs ? 'ma-7 pa-4' : ''"
      rounded="xl"
      color="rgb(0,0,0,0)"
      elevation="0"
    >
      <v-row no-gutters align="center">
        <v-col cols="12" sm="12" md="5" lg="6" xl="6">
          <!-- <v-avatar size="250" rounded="0">
            <v-img src="@/assets/posterImg.png" cover />
          </v-avatar> -->
          <Vue3Lottie
            animationLink="https://assets2.lottiefiles.com/packages/lf20_w51pcehl.json"
          />
        </v-col>
        <v-col cols="12" sm="12" md="7" lg="6" xl="6">
          <v-card color="rgb(0,0,0,0)" elevation="0">
            <v-card-title>
              <span class="text-h6">Oi, eu sou</span>
              <v-row
                class="text-h3 text-sm-h2 text-md-h2 text-lg-h2"
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
              <v-btn prepend-icon="mdi-linkedin" variant="plain" size="large"
                >Linkedin</v-btn
              >
              <v-btn prepend-icon="mdi-github" variant="plain" size="large"
                >GitHub</v-btn
              >
            </v-card-actions>
          </v-card>
          <v-row no-gutters class="px-4">
            <span>Seja muito bem vindo ao meu portfólio.</span>
          </v-row>
        </v-col>
      </v-row>
    </v-card>
  </v-responsive>
  <v-row no-gutters justify="center">
    <Vue3Lottie
      animationLink="https://assets2.lottiefiles.com/packages/lf20_x1kgpavt.json"
      :height="80"
      :width="80"
    />
  </v-row>
  <v-responsive id="aboutMe" min-height="100vh" class="align-center">
    <v-img
      v-if="!useDisplay.smAndDown"
      src="@/assets/img1.jpg"
      height="100vh"
      cover
    >
      <v-sheet
        color="rgb(0,0,0,0.8)"
        height="100vh"
        elevation="0"
        class="d-flex flex-row align-end"
      >
        <v-card color="rgb(0,0,0,0.5)" width="100vw" elevation="0">
          <v-row no-gutters align="center">
            <v-col cols="12" sm="12" md="4" lg="3" xl="3">
              <v-img
                src="@/assets/img2.jpg"
                min-height="400"
                max-height="400"
                cover
              />
            </v-col>
            <v-col cols="12" sm="12" md="8" lg="9" xl="9">
              <v-card color="rgb(0,0,0,0)" elevation="0" class="mx-auto">
                <v-card-title :class="!useDisplay.xs ? '' : 'text-center'">
                  <span :class="!useDisplay.xs ? 'text-h2' : 'text-h3'"
                    >Sobre mim</span
                  >
                </v-card-title>

                <v-card-text class="mt-2 text-subititle-1">
                  <v-row v-if="!useDisplay.xs" align="center">
                    <v-col cols="2" sm="2" md="1" lg="1" xl="1">
                      <v-row no-gutters align="center" justify="center">
                        <v-icon icon="mdi-hand-peace" size="60"></v-icon>
                      </v-row>
                    </v-col>
                    <v-col>
                      <span>
                        Prazer em conhecer, sou mais um apaixonado por
                        tecnologia, me considero uma pessoa autodidatica que
                        corre atrás para aprender o mais rapido possivel.
                        Atualmente casado e não possuo filhos.
                      </span>
                    </v-col>
                  </v-row>
                  <v-card v-else variant="outlined" class="pa-5" rounded="xl">
                    <v-row no-gutters align="center" justify="center">
                      <v-icon icon="mdi-hand-peace" size="80"></v-icon>
                      <p class="text-center">
                        Prazer em conhecer, sou mais um apaixonado por
                        tecnologia me considero uma pessoa autodidatica que
                        corri atrás para aprender o mais rapido possivel.
                        Atualmente casado e não possuo filhos.
                      </p>
                    </v-row>
                  </v-card>
                  <v-row v-if="!useDisplay.xs" align="center">
                    <v-col cols="2" sm="2" md="1" lg="1" xl="1">
                      <v-row no-gutters align="center" justify="center">
                        <v-icon icon="mdi-school" size="60"></v-icon>
                      </v-row>
                    </v-col>
                    <v-col>
                      <span>
                        Sempre fui muito apaixonado pela tecnologia, desmontava
                        tudo o que via pela frente e por conta disso me
                        aprofundei na area de manutenção de hardware realizando
                        um curso
                        <strong class="text-blue">Técnico em TI</strong>.
                        <br />
                        Logo após obtive meu primeiro contato com a programação
                        atraves do VBA ( Visual Basic Applications ) realizando
                        automatizações em planilhas assim atualmente estou
                        realizando a faculdade
                        <strong class="text-blue"
                          >Desenvolvimento de Software Multi Plataforma</strong
                        >
                      </span>
                    </v-col>
                  </v-row>
                  <v-card
                    v-else
                    variant="outlined"
                    class="pa-5 mt-3"
                    rounded="xl"
                  >
                    <v-row align="center" justify="center">
                      <v-icon icon="mdi-school" size="80"></v-icon>
                      <p>
                        Sempre fui muito apaixonado pela tecnologia, desmontava
                        tudo o que via pela frente e por conta disso me
                        aprofundei na area de manutenção de hardware realizando
                        um curso
                        <strong class="text-blue">Técnico em TI</strong>.
                        <br />
                        Logo após obtive meu primeiro contato com a programação
                        atraves do VBA ( Visual Basic Applications ) realizando
                        automatizações em planilhas assim atualmente estou
                        realizando a faculdade
                        <strong class="text-blue"
                          >Desenvolvimento de Software Multi Plataforma</strong
                        >
                      </p>
                    </v-row>
                  </v-card>
                  <v-row v-if="!useDisplay.xs" align="center">
                    <v-col cols="2" sm="2" md="1" lg="1" xl="1">
                      <v-row no-gutters align="center" justify="center">
                        <v-icon icon="mdi-google-downasaur" size="60"></v-icon>
                      </v-row>
                    </v-col>
                    <v-col>
                      <span>
                        Sou um gamer, e como todo gamer o nosso passa tempo
                        preferido é jogar. Gosto de jogos como Valorant, League
                        of Legends entre outros. Meu Jogo preferido é Resident
                        Evil, sou um fã da saga Resident Evil.
                      </span>
                    </v-col>
                  </v-row>
                  <v-card
                    v-else
                    variant="outlined"
                    class="pa-5 mt-3"
                    rounded="xl"
                  >
                    <v-row align="center" justify="center">
                      <v-icon
                        icon="mdi-google-downasaur"
                        size="80"
                        class="my-2"
                      ></v-icon>
                      <p class="text-center">
                        Sou um gamer, e como todo gamer o nosso passa tempo
                        preferido é jogar. Gosto de jogos como Valorant, League
                        of Legends entre outros. Meu Jogo preferido é Resident
                        Evil, sou um fã da saga Resident Evil.
                      </p>
                    </v-row>
                  </v-card>
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-card>
      </v-sheet>
    </v-img>
    <v-card v-else color="rgb(0,0,0,0.5)" width="100vw" elevation="0">
      <v-row no-gutters align="center">
        <v-col cols="12" sm="12" md="4" lg="3" xl="3">
          <v-img
            src="@/assets/img2.jpg"
            min-height="400"
            max-height="600"
            cover
          />
        </v-col>
        <v-col cols="12" sm="12" md="8" lg="9" xl="9">
          <v-card color="rgb(0,0,0,0)" elevation="0" class="mx-auto">
            <v-card-title :class="!useDisplay.xs ? '' : 'text-center'">
              <span :class="!useDisplay.xs ? 'text-h2' : 'text-h3'"
                >Sobre mim</span
              >
            </v-card-title>

            <v-card-text class="mt-2 text-subititle-1">
              <v-row v-if="!useDisplay.xs" align="center">
                <v-col cols="2" sm="2" md="1" lg="1" xl="1">
                  <v-row no-gutters align="center" justify="center">
                    <v-icon icon="mdi-hand-peace" size="60"></v-icon>
                  </v-row>
                </v-col>
                <v-col>
                  <span>
                    Prazer em conhecer, sou mais um apaixonado por tecnologia,
                    me considero uma pessoa autodidatica que corre atrás para
                    aprender o mais rapido possivel. Atualmente casado e não
                    possuo filhos.
                  </span>
                </v-col>
              </v-row>
              <v-card v-else variant="outlined" class="pa-5 mr-3" rounded="xl">
                <v-row no-gutters align="center" justify="center">
                  <v-icon icon="mdi-hand-peace" size="80"></v-icon>
                  <p class="text-center">
                    Prazer em conhecer, sou mais um apaixonado por tecnologia me
                    considero uma pessoa autodidatica que corri atrás para
                    aprender o mais rapido possivel. Atualmente casado e não
                    possuo filhos.
                  </p>
                </v-row>
              </v-card>
              <v-row v-if="!useDisplay.xs" align="center">
                <v-col cols="2" sm="2" md="1" lg="1" xl="1">
                  <v-row no-gutters align="center" justify="center">
                    <v-icon icon="mdi-school" size="60"></v-icon>
                  </v-row>
                </v-col>
                <v-col>
                  <span>
                    Sempre fui muito apaixonado pela tecnologia, desmontava tudo
                    o que via pela frente e por conta disso me aprofundei na
                    area de manutenção de hardware realizando um curso
                    <strong class="text-blue">Técnico em TI</strong>.
                    <br />
                    Logo após obtive meu primeiro contato com a programação
                    atraves do VBA ( Visual Basic Applications ) realizando
                    automatizações em planilhas assim atualmente estou
                    realizando a faculdade
                    <strong class="text-blue"
                      >Desenvolvimento de Software Multi Plataforma</strong
                    >
                  </span>
                </v-col>
              </v-row>
              <v-card v-else variant="outlined" class="pa-5 mt-3 mr-3" rounded="xl">
                <v-row align="center" justify="center">
                  <v-icon icon="mdi-school" size="80"></v-icon>
                  <p>
                    Sempre fui muito apaixonado pela tecnologia, desmontava tudo
                    o que via pela frente e por conta disso me aprofundei na
                    area de manutenção de hardware realizando um curso
                    <strong class="text-blue">Técnico em TI</strong>.
                    <br />
                    Logo após obtive meu primeiro contato com a programação
                    atraves do VBA ( Visual Basic Applications ) realizando
                    automatizações em planilhas assim atualmente estou
                    realizando a faculdade
                    <strong class="text-blue"
                      >Desenvolvimento de Software Multi Plataforma</strong
                    >
                  </p>
                </v-row>
              </v-card>
              <v-row v-if="!useDisplay.xs" align="center">
                <v-col cols="2" sm="2" md="1" lg="1" xl="1">
                  <v-row no-gutters align="center" justify="center">
                    <v-icon icon="mdi-google-downasaur" size="60"></v-icon>
                  </v-row>
                </v-col>
                <v-col>
                  <span>
                    Sou um gamer, e como todo gamer o nosso passa tempo
                    preferido é jogar. Gosto de jogos como Valorant, League of
                    Legends entre outros. Meu Jogo preferido é Resident Evil,
                    sou um fã da saga Resident Evil.
                  </span>
                </v-col>
              </v-row>
              <v-card v-else variant="outlined" class="pa-5 mt-3 mr-3" rounded="xl">
                <v-row align="center" justify="center">
                  <v-icon
                    icon="mdi-google-downasaur"
                    size="80"
                    class="my-2"
                  ></v-icon>
                  <p class="text-center">
                    Sou um gamer, e como todo gamer o nosso passa tempo
                    preferido é jogar. Gosto de jogos como Valorant, League of
                    Legends entre outros. Meu Jogo preferido é Resident Evil,
                    sou um fã da saga Resident Evil.
                  </p>
                </v-row>
              </v-card>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-card>
  </v-responsive>
  <v-responsive
    id="projects"
    height="100vh"
    class="align-center justify-center"
  >
    <v-card class="pa-5">
      <v-card-title class="text-h3 font-weight-bold text-center"
        >PROJETOS</v-card-title
      >
      <v-card-text class="mt-4">
        <v-row align="center">
          <v-col
            v-for="project in projects"
            :key="project"
            cols="12"
            sm="12"
            md="6"
            lg="3"
            xl="3"
          >
            <v-card
              color="grey-darken-2"
              width="100%"
              height="35vh"
              rounded="xl"
              elevation="0"
            >
              <v-img :src="project.image" cover>
                <v-card height="100%" color="rgb(0,0,0,0.5)">
                  <v-card-title class="text-h4">{{
                    project.name
                  }}</v-card-title>
                  <v-card-subtitle>
                    {{ project.sub }}
                  </v-card-subtitle>
                  <v-card-text class="text-body-1">{{
                    project.text
                  }}</v-card-text>
                </v-card>
                <v-card-actions class="mt-n16 mr-2">
                  <v-spacer></v-spacer>

                  <v-btn
                    :href="project.url"
                    target="_blank"
                    prepend-icon="mdi-link"
                    variant="outlined"
                    >Visualizar</v-btn
                  >
                </v-card-actions>
              </v-img>
              <!-- <v-sheet
                  color="blue"
                  class="mt-1 mr-8 float-end"
                  width="100%"
                  style="transform: rotate(-28deg)"
                >
                  <span class="ml-12 text-h5">{{ projeto.name }}</span>
                </v-sheet> -->
            </v-card>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
  </v-responsive>
</template>

<script>
import { Vue3Lottie } from "vue3-lottie";
import { useDisplay } from "vuetify";
export default {
  components: {
    Vue3Lottie,
  },
  data() {
    return {
      useDisplay: useDisplay(),
      name: "Raul Silva Araujo",
      animatedName: "",
      iconVisible: true,
      isActive: false,
      projects: [
        {
          name: "Multi Plus Streaming",
          sub: "Vue.Js, Vuetify, Vue Router, Pinia e Vite.",
          text: "Site de filmes, series e livros que permita aos usuários realizarem um cadastro, adicionar suas obras favoritas em uma lista personalizada, consultar informações, marcar os assistidos/lidos e verificar em qual plataforma o mesmo estará disponivel.",
          url: "https://multi-plus-streaming.vercel.app/",
          image:
            "https://front-3t5xttaqp-raulsaraujo.vercel.app/assets/Backgroud.6f70cb0d.png",
        },
      ],
    };
  },
  mounted() {
    this.animateName();
    setInterval(() => {
      this.iconVisible = !this.iconVisible;
    }, 1000);
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
    scrollById(id) {
      const el = document.getElementById(id);
      const elCoordenadas = el.getBoundingClientRect();
      window.scrollBy(elCoordenadas.x, elCoordenadas.y);
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
