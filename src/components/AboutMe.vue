<template>
  <v-app class="align-center">
    <v-img
      v-if="!useDisplay.smAndDown"
      src="@/assets/img/img1.jpg"
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
                src="@/assets/img/img2.jpg"
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
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-card>
      </v-sheet>
    </v-img>
    <v-card v-else width="100vw" elevation="0" color="black">
      <v-row no-gutters align="center">
        <v-col cols="12" sm="12" md="4" lg="3" xl="3">
          <v-img
            src="@/assets/img/img2.jpg"
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

            <v-card-text class="mt-2 mr-5 text-subititle-1">
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
              <v-card
                v-else
                variant="outlined"
                class="pa-5 mt-3 mr-3"
                rounded="xl"
              >
                <v-row align="center" justify="center">
                  <v-icon icon="mdi-school" size="80"></v-icon>
                  <p class="text-center">
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
              <v-card
                v-else
                variant="outlined"
                class="pa-5 mt-3 mr-3"
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
  </v-app>
</template>

<script>
import { useDisplay } from "vuetify";
export default {
  data() {
    return {
      useDisplay: useDisplay(),
    };
  },
  methods: {},
};
</script>

<style>
</style>