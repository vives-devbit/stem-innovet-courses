<template>
  <v-card hover class="d-flex flex-column" height="100%" :href="course.site" target="_blank">
    <v-card flat tile class="">
      <v-img class="white--text align-end" :src="course.image" max-height="150" ></v-img>
    </v-card>

    <v-card flat tile class="flex">
      <v-card-title>{{ course.title }}</v-card-title>
      <v-card-subtitle>door {{ course.author }}</v-card-subtitle>

      <v-card-text class="text--primary">
        <div>{{ course.description }}</div>
      </v-card-text>
    </v-card>

    <v-card flat tile class="mx-4">

      <v-chip class="ma-2" color="secondary" text-color="white" v-if="course.time.theory">
        {{ course.time.theory }} theorie <v-icon right>mdi-book-open-page-variant</v-icon>
      </v-chip>

      <v-chip class="ma-2" color="secondary" text-color="white" v-if="course.time.lab">
        {{ course.time.lab }} labo <v-icon right>mdi-worker</v-icon>
      </v-chip>

      <v-chip class="ma-2" color="secondary" text-color="white" v-if="course.time.exercises">
        {{ course.time.exercises }} exercises <v-icon right>mdi-arm-flex-outline</v-icon>
      </v-chip>

    </v-card>

    <v-divider class="mx-4"></v-divider>

    <v-card tile flat class="mx-4">
      <v-row>
        <v-col cols="6">
          <v-btn color="primary" text :href="course.site" target="_blank" block>
            <v-icon>mdi-web</v-icon>&nbsp;Cursus
          </v-btn>
        </v-col>
        <v-col cols="6">
          <v-btn color="green" text :href="course.github" target="_blank" block>
            <v-icon>mdi-github-circle</v-icon>&nbsp;Github
          </v-btn>
        </v-col>
      </v-row>
    </v-card>
  </v-card>
</template>

<script>
export default {
  props: ['course']
}
</script>