<template>
  <v-app>
    <v-main>
      <hero-section></hero-section>
    </v-main>
  </v-app>
</template>

<script>
import HeroSection from "@/components/HeroSection";

export default {
  name: 'App',

  components: {
    HeroSection
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
  }
</style>
