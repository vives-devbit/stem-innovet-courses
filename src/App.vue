<template>
  <v-app>
    <div>
      <v-app-bar
        dark
        elevation="12"
        class="secondary darken-2"
      >
        <v-toolbar-title>Cursusmateriaal rond IoT voor STEM-richtingen uit de 3de graad SO</v-toolbar-title>
  
        <v-spacer></v-spacer>
  
        <v-btn
          color="red"
          class="ma-2 white--text"
          @click="$vuetify.goTo('#course_overview', 0, 2000)"
        >
          Courses
          <v-icon right dark>mdi-notebook-multiple</v-icon>
        </v-btn>
  
      </v-app-bar>
    </div>

    <v-content>
      <v-img src="./assets/iot_technology.jpg" max-height="400"></v-img>
      <CorePoints />

      <v-container id="course_overview">
        <v-container v-for="category in courses" :key="category.category">
          <CourseOverview :courses="category.courses" :title="category.category"/>
        </v-container>
      </v-container>
    </v-content>
    <Footer/>

  </v-app>
</template>

<script>
import CourseOverview from './components/CourseOverview';
import Footer from './components/Footer';
import CorePoints from './components/CorePoints';
import courses from './data/courses.json';

export default {
  name: 'App',

  components: {
    CourseOverview,
    Footer,
    CorePoints,
  },

data: () => ({
    courses: courses
  }),
};
</script>
