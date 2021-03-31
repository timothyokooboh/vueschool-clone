<template>
  <v-app>
    <v-main>
      <hero-section></hero-section>
      <vue-school-courses></vue-school-courses>
      <more-lessons></more-lessons>
      <vue-school-teachers></vue-school-teachers>
      <vue-school-benefits></vue-school-benefits>
      <the-footer></the-footer>
    </v-main>
  </v-app>
</template>

<script>
import HeroSection from "@/components/HeroSection";
import VueSchoolCourses from './components/VueSchoolCourses.vue';
import MoreLessons from './components/MoreLessons.vue';
import VueSchoolTeachers from "./components/VueSchoolTeachers";
import VueSchoolBenefits from "./components/VueSchoolBenefits";
import TheFooter from "./components/TheFooter";

export default {
  name: 'App',

  components: {
    HeroSection,
    VueSchoolCourses,
    MoreLessons,
    VueSchoolTeachers,
    VueSchoolBenefits,
    TheFooter,
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
