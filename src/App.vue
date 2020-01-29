<template>
  <v-app>
    <div>
      <v-app-bar
        dark
        elevation="12"
      >
        <v-toolbar-title>IoT, slimme school 2.0 </v-toolbar-title>
  
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
      <CorePoints />
      <CourseOverview :courses="courses"/>
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
