<script setup lang="ts">
const socialMedia = [
  { icon: 'mdi-facebook', url: 'https://www.facebook.com/VTI-Torhout-247139098672850/' },
  { icon: 'mdi-twitter', url: 'https://twitter.com/VtiTorhout' },
  { icon: 'mdi-instagram', url: 'https://www.instagram.com/vti_torhout' },
];

const logos = [
  { image: "./img/logo_vives.png", site: "https://www.vives.be" },
  { image: "./img/logo_MCT.jpg", site: "https://www.howest.be/nl/opleidingen/bachelor/multimedia-en-creatieve-technologie" },
  { image: "./img/logo_vti.jpg", site: "https://vti.sint-rembert.be/" },
  { image: "./img/logo_vla_oo.jpg", site: "https://onderwijs.vlaanderen.be/" },
  { image: "./img/logo_innovet.jpeg", site: "#" },
];
</script>

<template>
  <v-footer
    color="ternary"
  >

    <v-row dense>
      
      <v-col cols="12" sm="4">
        <v-card flat class="bg-ternary">
          <v-card-text class="text-center">
            De inhoud van STEM-ICT.be werd opgezet door VTI-Torhout in samenwerking met hogescholen VIVES en HoWest en met steun van InnoVET van het Departement Onderwijs en Vorming. InnoVET wil inzetten op de ondersteuning en professionalisering van leerkrachten PV/TV, via duurzame trajecten in samenwerking met partners uit het arbeidsveld.
          </v-card-text>
          <v-container class="d-flex flex-wrap justify-center">
            <a
              v-for="(logo, i) in logos"
              :key="`logo_${i}`"
              :href="logo.site" target="_blank"
              class="ma-2"
            >
              <v-img :src="logo.image" aspect-ratio="1" height="96" width="96" class="rounded-lg" />
            </a>
          </v-container>
        </v-card>
      </v-col>
      
      <v-col cols="12" sm="4">
        <v-card class="bg-ternary text-center" flat>
          <v-card-text class="text-center">
            Contacteer ons via sociale media
          </v-card-text>
          <div class="mt-2">
            <v-btn
              v-for="media in socialMedia"
              :key="media.icon"
              class="text-white bg-ternary mx-4"
              icon flat
              :href="media.url"
              target="_blank"
            >
              <v-icon size="48px">{{ media.icon }}</v-icon>
            </v-btn>
          </div>
          <v-card-text class="mt-4 text-center">
            of via mail
          </v-card-text>
          <div class="mt-2 d-flex justify-center">
            <v-card class="bg-ternary-lighten-2 rounded-pill d-flex justify-center align-center ma-0 py-0" href="mailto:kris.werbrouck@sint-rembert.be">
              <v-avatar start size="large">
                <v-img src="./img/kris_werbrouck.jpg"></v-img>
              </v-avatar>
              <div class="mx-4">
                <div class="font-weight-black">Kris Werbrouck</div>
                <div>Leerkracht VTI Torhout</div>
              </div>
            </v-card>
          </div>
        </v-card>
      </v-col>
      
      <v-col cols="12" sm="4">
        <v-card class="text-center bg-ternary" flat>
          <v-card-text>
            Een website gebracht door
          </v-card-text>
          <div class="mt-2">
            <a href="https://www.vives.be" target="_blank"><v-img src="./img/devbit.png" max-height="160" contain></v-img></a>
          </div>
        </v-card>
      </v-col>
    </v-row>

  </v-footer>
</template>