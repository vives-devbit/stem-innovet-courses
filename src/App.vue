<script setup lang="ts">
import hero from '@/assets/iot_technology.jpg'
import CorePoints from '@/components/CorePoints.vue'
import BottomFooter from '@/components/BottomFooter.vue';
import CourseOverview from '@/components/CourseOverview.vue';

import courses from './data/courses.json';

</script>

<template>
  <v-app>
    <v-app-bar flat class="bg-ternary" density="comfortable">
      <v-app-bar-title class="text-subtitle-1">Cursusmateriaal rond IoT voor STEM-richtingen uit de 3de graad SO</v-app-bar-title>
      <v-spacer></v-spacer>
      <v-btn class="bg-red">
        Courses
        <v-icon end icon="mdi-notebook-multiple"></v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-img :src="hero" cover max-height="360"></v-img>
      <CorePoints />

      <!-- <v-container id="course_overview"> -->
        <div v-for="category in courses" :key="category.category">
          <CourseOverview :courses="category.courses" :title="category.category"/>
        </div>
      <!-- </v-container> -->
    </v-main>

    <BottomFooter />
  </v-app>
</template>
