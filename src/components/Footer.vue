<template>
  <v-footer
    dark
    color="secondary darken-2"
  >

    <v-row>
      
      <v-col cols="12" sm="4">
        <v-card color="secondary darken-2" tile flat>
          <v-card-title>IoT, slimme school 2.0.</v-card-title>
          <v-card-text>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed vel libero luctus, pretium nunc sed, varius mauris. Aliquam fringilla, diam a scelerisque auctor, sapien sem consectetur lectus, et vestibulum sapien odio ac quam. Morbi fermentum gravida nisl, laoreet venenatis velit bibendum eget. Nunc interdum eu quam a hendrerit. Proin laoreet metus vitae ultricies eleifend.
          </v-card-text>
          <v-card-text>
            In nisl mauris, porttitor quis ex non, feugiat pellentesque massa. Sed vel feugiat sapien. Nam felis nibh, lacinia et metus in, bibendum maximus turpis. Donec in quam tellus. Donec feugiat scelerisque massa non faucibus. Etiam arcu urna, ultricies at cursus nec, aliquet quis lacus.
          </v-card-text>
        </v-card>
      </v-col>
      
      <v-col cols="12" sm="4">
        <v-card color="secondary darken-2" tile flat>
          <v-card-text>
            Dit project is een samenwerking tussen VTI Torhout en de VIVES hogeschool.
          </v-card-text>
          <v-container fluid>
            <v-row>
              <v-col
                v-for="logo in logos"
                :key="logo"
                class="d-flex child-flex"
                cols="3"
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
        <v-card class="white--text text-center pa-3"  color="secondary darken-2" tile flat>
          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4"
            icon
          >
            <v-icon size="32px">{{ icon }}</v-icon>
          </v-btn>

        </v-card>
      </v-col>
      
      <v-divider></v-divider>
  
      <v-card
        class="flex"
        tile flat color="secondary darken-2"
      >
        <v-card-text class="py-2 white--text text-center">
          Een website gebracht door <a href="https://www.devbit.be">DevBit</a>
        </v-card-text>
      </v-card>
    </v-row>

  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: [
      'mdi-facebook',
      'mdi-twitter',
      'mdi-google-plus',
      'mdi-linkedin',
      'mdi-instagram',
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
</style>