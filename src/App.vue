<template>
  <v-app>
    <v-main>
      <hero-section></hero-section>
      <div 
        class="py-16"
        style="background: #EDF3FF"
      >
        <div class="text-center display-2 pb-4"> Some of our awesome courses </div>
        <div class="text-center display-1">420 lessons • 31 Hours • 28 Courses</div>
        <div class="text-center mt-4 mb-16">
          <v-btn 
            outlined 
            color="#F63F75"
            class="title"
          >
            new content added weekly
          </v-btn>
        </div>

        <div class="d-flex flex-wrap justify-center ml-3">
          <v-card
            v-for="course in courses"
            :key="course.title"
            class="mr-3 mb-8 rounded-lg"
            max-width="400"
            style="position: relative;"
          >
            <v-avatar 
              tile 
              width="100%" 
              height="200"
              style="position: relative;"
              class="rounded-t-lg"
            >
              <v-img :src="course.image"></v-img>
            </v-avatar>
            <div 
              style="position: absolute; top: 20px; left: 10px;"
              class="d-flex"
            >
              <div
                v-for="(label, index) in course.labels"
                :key="index"
                :class="{'in-progress': label === 'in progress', 'free': label === 'free', 'premium': label === 'premium'}"
                class="rounded-lg py-1 px-3 mr-2 title text-uppercase"
              >
                {{label}}
              </div>
            </div>
            <div 
              class="px-4 py-2"
              style="color: #766B93"
            >
              <div class="display-1 text-capitalize pb-4 font-weight-medium">{{course.title}}</div>
              <div class="d-flex align-center pb-4">
                <div class="pr-3">
                  <img 
                    src="./assets/runtime.png" 
                    alt="clock" 
                    class="pt-1"
                    style="width: 2.5rem"
                  >
                </div>
                <div class="pr-3">{{course.duration}} </div>
                <div class="pr-3">|</div>
                <div>{{course.numberOfLessons}} lessons</div>
              </div>
              <div class="headline mb-16">
                {{course.description}}
              </div>
              <div 
                class="text-uppercase title ml-4 py-1 px-2 mb-3"
                style="position: absolute; bottom: 0; left: 0; background: #EAE9EF"
              >
                {{course.difficulty}}
              </div>
            </div>
          </v-card>
        </div>

        <div class="text-center mt-8">
          <v-btn color="#4DC3A0" class="rounded-pill py-8 px-12 display-1 white--text mb-4">see all our courses</v-btn>
          <div>
            <span style="color: #F63F75">Learn Vue.js</span> <span class="font-weight-bold grey--text text--darken-2 ">for $25/month or $190/year</span>
          </div>
        </div>
      </div>

      <div
        class="py-16 px-4"
        style="background: #E6EDFC"
      >
          <div class="display-1">Featured lessons</div>
      </div>
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
    courses: [
      {
        image: require("./assets/hero-image.jpg"),
        labels: ["in progress", "premium"],
        title: "the vue.js 3 masterclass",
        duration: "3hrs",
        numberOfLessons: 52,
        extra: "More lessons coming soon",
        description: "Learn how to build real-world application with vue.js 3 in the supercharged and remastered vue.js masterclass.",
        difficulty: "intermediate"
      },
      {
        image: require("./assets/nuxtjs-fundamentals.jpeg"),
        labels: ["free"],
        title: "Nuxt.js fundamentals",
        duration: "35min",
        numberOfLessons: 14,
        description: "Learn the fundamentals of nuxtjs in this course that we created together with the founders of Nuxt. The course covers wht you need to know f...",
        difficulty: "beginner"
      },
      {
        image: require("./assets/learn-how-to-test-vuejs-components.jpeg"),
        labels: ["premium"],
        title: "Testing vue.js components",
        duration: "1hr",
        numberOfLessons: 11,
        description: "Learn everything you need to test your vue.js components like a pro!",
        difficulty: "advanced"
      },
      {
        image: require("./assets/vuejs-form-validation.jpeg"),
        labels: ["premium"],
        title: "Vue.js form validation",
        duration: "34min",
        numberOfLessons: 12,
        description: "Learn how to validate your forms with vue.js and vuelidate like a pro!",
        difficulty: "intermediate"
      },
      {
        image: require("./assets/vuex-for-everyone.jpeg"),
        labels: ["free"],
        title: "Vuex for everyone",
        duration: "1hr",
        numberOfLessons: 16,
        description: "This vue.js course is based on the official vuex example. We will create a shopping cart with vue and progressively discover and learn about vue ...",
        difficulty: "advanced"
      },
      {
        image: require("./assets/vuejs-components-fundamentals.jpeg"),
        labels: ["free"],
        title: "Vue.js components fundamentals",
        duration: "53min",
        numberOfLessons: 11,
        description: "Components are the puzzle pieces of a vue.js website. Learn the fundamental concept of vue.js components in this course",
        difficulty: "beginner"
      }
    ],
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

  .in-progress {
    background-color: #fff;
  }
  .free {
    background-color: #667DFF;
    color: #fff;
  }
  .premium {
    background-color: #FF3DA8;
    color: #fff;
  }
</style>
