<template>
  <v-app>
      <v-app-bar
        dark
      >
        <v-toolbar-title>IoT, slimme school 2.0 </v-toolbar-title>
  
        <v-spacer></v-spacer>
  
        <v-btn
          color="red"
          class="ma-2 white--text"
        >
          Courses
          <v-icon right dark>mdi-notebook-multiple</v-icon>
        </v-btn>
  
      </v-app-bar>

    <v-content>
      <Course />
      <Course />
    </v-content>
    <Footer/>

  </v-app>
</template>

<script>
import Course from './components/Course';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    Course,
    Footer,
  },

  data: () => ({
    //
  }),
};
</script>
