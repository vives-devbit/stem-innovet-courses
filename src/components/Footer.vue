<template>
  <v-footer
    dark
    color="secondary darken-2"
  >

    <v-row>
      
      <v-col cols="12" sm="4">
        <v-card color="secondary darken-2" tile flat>
          <v-card-text>
            STEM-ICT.be werd opgezet door VTI-Torhout en hogeschool VIVES met steun van InnoVET van het Departement Onderwijs en Vorming. InnoVET wil inzetten op de ondersteuning en professionalisering van leerkrachten PV/TV, via duurzame trajecten in samenwerking met partners uit het arbeidsveld.
          </v-card-text>
          <v-container fluid>
            <v-row justify="center">
              <v-col
                v-for="logo in logos"
                :key="logo"
                class="d-flex child-flex"
                cols="4"
                sm="6"
                md="4"
                lg="3"
                xl="2"
              >
                <v-card flat tile color="secondary" class="d-flex round-card darken-2">
                  <v-img
                    :src="logo"
                    aspect-ratio="1"
                    contain
                  >

                  </v-img>
                </v-card>
              </v-col>
            </v-row>
          </v-container>
        </v-card>
      </v-col>
      
      <v-col cols="12" sm="4">
        <v-card class="white--text text-center"  color="secondary darken-2" tile flat>
          <div class="mt-4">
            <v-btn
              v-for="media in social_media"
              :key="media.icon"
              class="mx-4"
              icon
              :href="media.url"
              target="_blank"
            >
              <v-icon size="48px">{{ media.icon }}</v-icon>
            </v-btn>
          </div>
          <div class="mt-8">
            <v-chip
              pill
              class="ma-2"
              v-on="on"
              large
              href="mailto:kris.werbrouck@sint-rembert.be"
            >
              <v-avatar left class="contact">
                <v-img src="/img/kris_werbrouck.jpg"></v-img>
              </v-avatar>
              <span class="font-weight-black pa-4">Kris Werbrouck</span>
            </v-chip>
          </div>
        </v-card>
      </v-col>
      
      <v-col cols="12" sm="4">
        <v-card class="white--text text-center"  color="secondary darken-2" tile flat>
          <v-card-text>
            Een website gebracht door
          </v-card-text>
          <a href="https://www.devbit.be" target="_blank"><v-img src="../assets/devbit.png" max-height="160" contain></v-img></a>
        </v-card>
      </v-col>
    </v-row>

  </v-footer>
</template>

<script>
export default {
  data: () => ({
    social_media: [
      {icon: 'mdi-facebook', url: 'https://www.facebook.com/VTI-Torhout-247139098672850/'},
      {icon: 'mdi-twitter', url: 'https://twitter.com/VtiTorhout'},
      {icon: 'mdi-instagram', url: 'https://www.instagram.com/vti_torhout'},
    ],
    logos: [
      "https://www.vives.be/sites/default/files/thumbnails/image/Logo-VIVES.png",
      "https://pbs.twimg.com/profile_images/1168805095305359362/nd_w3xch_400x400.jpg",
      "https://www.klascement.net/organisations/1/9/6/l/ovla_2.jpg",
      "http://www.technischatheneumkeerbergen.be/wp-content/uploads/2019/12/fullsizeoutput_1d83.jpeg",
    ]
  }),
};
</script>

<style scoped>
.round-card {
  border-radius: 10%;
}
.contact {
  height: 52px !important;
  width: 52px !important;
}
</style>