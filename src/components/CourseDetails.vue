<script setup lang="ts">
  const props = defineProps({
    course: { type: Object, required: true }
  })
</script>

<template>
  <v-card hover class="d-flex flex-column" height="100%" :href="props.course.site" target="_blank">
    <v-card flat>
      <v-img class="white--text align-end" :src="props.course.image" max-height="150" ></v-img>
    </v-card>

    <v-card flat class="flex">
      <v-card-title>{{ props.course.title }}</v-card-title>
      <v-card-subtitle>door {{ props.course.author }}</v-card-subtitle>

      <v-card-text class="text--primary">
        <div>{{ props.course.description }}</div>
      </v-card-text>
    </v-card>

    <v-card flat class="mx-4">

      <v-chip class="ma-2" color="secondary" text-color="white" v-if="props.course.time.theory">
        {{ props.course.time.theory }} theorie <v-icon right>mdi-book-open-page-variant</v-icon>
      </v-chip>

      <v-chip class="ma-2" color="secondary" text-color="white" v-if="props.course.time.lab">
        {{ props.course.time.lab }} labo <v-icon right>mdi-worker</v-icon>
      </v-chip>

      <v-chip class="ma-2" color="secondary" text-color="white" v-if="props.course.time.exercises">
        {{ props.course.time.exercises }} exercises <v-icon right>mdi-arm-flex-outline</v-icon>
      </v-chip>

    </v-card>

    <v-divider class="mx-4"></v-divider>

    <v-card flat class="mx-4">
      <v-container class="d-flex flex-row justify-center flex-wrap">
        <v-btn v-if="props.course.site" color="primary" text :href="props.course.site" target="_blank">
          <v-icon left>mdi-web</v-icon>Cursus
        </v-btn>
        <v-btn v-if="props.course.github" color="green" text :href="props.course.github" target="_blank">
          <v-icon left>mdi-github</v-icon>Github
        </v-btn>
        <v-btn v-if="props.course.youtube" color="red" text :href="props.course.youtube" target="_blank">
          <v-icon left>mdi-youtube</v-icon>Youtube
        </v-btn>
        <v-btn v-if="props.course.file" color="black" text :href="props.course.file" target="_blank">
          <v-icon left>mdi-file</v-icon>Document
        </v-btn>
      </v-container>
    </v-card>
  </v-card>
</template>