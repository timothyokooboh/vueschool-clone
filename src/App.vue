<template>
  <v-app>
    <v-main>
      <hero-section></hero-section>
      <vue-school-courses></vue-school-courses>
      <more-lessons></more-lessons>
    </v-main>
  </v-app>
</template>

<script>
import HeroSection from "@/components/HeroSection";
import VueSchoolCourses from './components/VueSchoolCourses.vue';
import MoreLessons from './components/MoreLessons.vue';

export default {
  name: 'App',

  components: {
    HeroSection,
    VueSchoolCourses,
    MoreLessons
  },

  data: () => ({
  }),
};
</script>

<style>
  :root {
    font-size: 62.5%; /* 1 rem = 10px */
  }

  body {
    font-size: 1.6rem;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
</style>
