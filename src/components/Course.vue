<template>
  <v-card class="mx-auto" max-width="400" hover=true>
    <v-img class="white--text align-end" src="http://www.picserver.org/highway-signs2/images/programming.jpg"></v-img>

    <v-card-title>{{ course.title }}</v-card-title>
    <v-card-subtitle>by {{ course.author }}</v-card-subtitle>

    <v-card-text class="text--primary">
      <div>This course aims to guide you to become a good programmer by teaching you the core concepts required for object oriented programming. While the language used here is C#, any or most other OOP programming languages can be used in combination with this course.</div>
    </v-card-text>

    <v-card-text>
      <v-chip class="ma-2" color="primary" text-color="white">
        6u theorie <v-icon right>mdi-book-open-page-variant</v-icon>
      </v-chip>

      <v-chip class="ma-2" color="secondary" text-color="white">
        12u labo <v-icon right>mdi-worker</v-icon>
      </v-chip>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>

    <v-card-actions>

      <v-btn color="green" text>
        <v-icon>mdi-web</v-icon>&nbsp;Course
      </v-btn>

      <v-btn color="blue" text>
        <v-icon>mdi-watch</v-icon>&nbsp;18 uur
      </v-btn>

      <v-btn color="orange" text>
        <v-icon>mdi-github-circle</v-icon>&nbsp;Github
      </v-btn>

    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: ['course']
}
</script>