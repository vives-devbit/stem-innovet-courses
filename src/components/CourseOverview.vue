<template>
  <v-container fluid>
    <v-row>
      <v-col class="course" v-for="course in courses" :key="course">
        <Course :course="course"/>
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
    courses: [
      { title: 'Learn to Program' },
      { title: 'God is dead' }
    ]
  }),
}
</script>

<style scoped>
</style>>