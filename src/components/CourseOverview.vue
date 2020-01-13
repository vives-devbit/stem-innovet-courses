<template>
  <v-row>
    <v-col class="course flex-grow-0" v-for="course in courses" :key="course">
      <Course/>
    </v-col>
  </v-row>
</template>

<script>
import Course from './Course';

export default {
  components: {
    Course,
  },
  
  data: () => ({
    courses: [1, 2, 3]
  }),
}
</script>

<style scoped>
</style>>