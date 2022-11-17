<script setup lang="ts">
  const coursProps = defineProps({
    course: { type: Object, required: true }
  })
</script>

<template>
  <v-hover>
    <template v-slot:default="{ isHovering, props }">
      <v-card v-bind="props" :elevation="isHovering ? 12 : 4" class="d-flex flex-column" height="100%" :href="coursProps.course.site" target="_blank">
        <v-card flat>
          <v-img :src="coursProps.course.image" max-height="150" ></v-img>
        </v-card>

        <v-card flat>
          <v-card-title>{{ coursProps.course.title }}</v-card-title>
          <v-card-subtitle>door {{ coursProps.course.author }}</v-card-subtitle>

          <v-card-text class="text-primary">
            <div>{{ coursProps.course.description }}</div>
          </v-card-text>
        </v-card>

        <v-divider class="mx-4 mt-auto"></v-divider>

        <v-card flat class="mx-4">
          <v-container class="d-flex flex-row justify-center">
            <v-btn v-if="coursProps.course.site" color="secondary" variant="text" :href="coursProps.course.site" target="_blank">
              <v-icon left>mdi-web</v-icon>Cursus
            </v-btn>
            <v-btn v-if="coursProps.course.github" color="green" variant="text" :href="coursProps.course.github" target="_blank">
              <v-icon left>mdi-github</v-icon>Github
            </v-btn>
            <v-btn v-if="coursProps.course.youtube" color="red" variant="text" :href="coursProps.course.youtube" target="_blank">
              <v-icon left>mdi-youtube</v-icon>Youtube
            </v-btn>
            <v-btn v-if="coursProps.course.file" color="black" variant="text" :href="coursProps.course.file" target="_blank">
              <v-icon left>mdi-file</v-icon>Document
            </v-btn>
          </v-container>
        </v-card>
      </v-card>
    </template>
  </v-hover>
</template>