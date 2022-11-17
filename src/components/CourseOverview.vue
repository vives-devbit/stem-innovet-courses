<script setup lang="ts">
import CourseDetails from '@/components/CourseDetails.vue';

const props = defineProps({
  courses: { type: [] as any, required: true },
  title: { type: String, required: true }
});

</script>

<template>
  <v-sheet>
    <v-row>
      <v-col cols="12" class="text-center bg-ternary">
        <h2 class="my-2">{{ props.title }}</h2>
      </v-col>
    </v-row>

    <v-container>
      <v-row class="my-6" justify="center">
        <v-col
          cols="12"
          sm="6"
          md="6"
          lg="4"
          xl="3"
          v-for="course in courses" :key="course.id">
            <CourseDetails :course="course"/>
        </v-col>
      </v-row>
    </v-container>
  </v-sheet>
</template>
