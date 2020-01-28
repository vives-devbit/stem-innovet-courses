<template>
  <v-container>
    <v-row>
      <v-col
        cols="12"
        sm="6"
        md="6"
        lg="4"
        xl="3"
        v-for="course in courses" :key="course.id">
          <Course :course="course"/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Course from './Course';

export default {
  props: ['courses'],
  components: {
    Course,
  },
}
</script>

<style scoped>
</style>>