<template>
  <v-container>
    <v-row>
      <v-col cols="12" fluid class="text-center title">
        <h2>{{title}}</h2>
      </v-col>
    </v-row>

    <v-row justify="center">
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
  props: ['courses', 'title'],
  components: {
    Course,
  },
}
</script>

<style scoped>
.title {
  color: white;
  background-color: #171717;
  padding: 24px;
  margin-top: 12px;
  margin-bottom: 12px;;
}
</style>>