<template>
  <v-container fluid>
    <v-row>
      <v-col class="course" v-for="course in courses" :key="course">
        <Course/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Course from './Course';

export default {
  components: {
    Course,
  },
  
  data: () => ({
    courses: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13]
  }),
}
</script>

<style scoped>
</style>>