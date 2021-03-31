<template>
    <div>
         <div
        style="background-color: #3A348D"
      >
        <div 
          class="d-flex align-center white--text px-6"
          style="height: 60vh"
        >
                
          <div 
            class="d-flex align-center justify-center"
            style="width: 100%"
          >
            <div>
              <div class="display-2 pb-4">Join our Vue.js community and get started for free:</div>
                <div class="d-flex align-center justify-center white">
                  <custom-input 
                    class="white"
                    color="white"
                    placeholder="Your Email"
                  >
                  </custom-input>
                  <div>
                    <v-btn 
                      class="headline white--text headline mr-2 py-6 px-8 font-bold"
                      color="#40B08E"
                    >
                      Start Learning Vue.js
                    </v-btn>
                  </div>
                 </div>
                </div>
              </div>
            </div>
          <div>
        </div>

        <img
          src="../assets/vueschool_logo_multicolor_negative.svg" 
          alt="vue school logo"
          style="margin-left: -10px"
        >
        <div 
          class="white--text px-4 py-4"
          style="max-width: 50rem"
        >
          <div class="pb-4"> Our goal is to be the number one source of Vue.js knowledge for all skill levels. We offer the knowledge of our industry leaders through awesome video courses for a ridiculously low price.</div>
          <div>More than 80.000 users have already joined us. You are welcome too!</div>
        </div>

        <div class="mx-4 pb-8 d-md-flex justify-space-between">
          <div class="pb-4">
            <a 
              href="https://web.facebook.com/vueschool/?_rdc=1&_rdr"  
              class="mr-4"
              style="text-decoration: none"
            >
              <v-icon color="white">mdi-facebook</v-icon>
            </a>
            <a 
              href="https://twitter.com/vueschool_io" 
              class="mr-4"
              style="text-decoration: none"
            >
                <v-icon color="white">mdi-twitter</v-icon>
            </a>
            <a 
              href="https://github.com/vueschool/"
              style="text-decoration: none"
            >
              <v-icon color="white">mdi-github</v-icon>
            </a>
          </div>

          <div class="d-md-flex">
            <div class="pr-2 pb-4">
              <a 
                href="https://vueschool.io/"
                style="text-decoration: none"
                class="white--text"
              >
                Home
              </a>
            </div>

            <div class="pr-2 pb-4">
               <a 
                href="https://vueschool.io/courses"
                style="text-decoration: none"
                class="white--text"
              >
                Courses
              </a>
            </div>

            <div class="pr-2 pb-4">
               <a 
                href="https://vueschool.io/plans"
                style="text-decoration: none"
                class="white--text pr-2 pb-2"
              >
                Plans
              </a>
            </div>

            <div class="pr-2 pb-4">
               <a 
                href="https://vueschool.io/tutorials"
                style="text-decoration: none"
                class="white--text pr-2 pb-2"
              >
                Tutorials
              </a>
            </div>

            <div class="pr-2 pb-4">
              <a 
                href="https://vueschool.io/workshops"
                style="text-decoration: none"
                class="white--text"
              >
                Workshops
              </a>
            </div>

            <div class="pr-2 pb-4">
              <a 
                href="https://vueschool.io/the-vuejs-master-class/"
                style="text-decoration: none"
                class="white--text"
              >
                Masterclass
              </a>
            </div>

            <div>
              <a 
                href="https://vueschool.io/affiliates"
                style="text-decoration: none"
                class="white--text"
              >
                Affiliate program
              </a>
            </div>
          </div>
        </div>

        <div 
          class="d-md-flex justify-space-between align-center px-4"
          style="background: #1D185E"
        >
          <div class="white--text py-2">
            © All rights reserved. Cloned with ❤️ by <a href="https://timothyokooboh.github.io/portfolio" style="text-decoration: none; color: white">timothy</a>.
          </div>
          <div class="white--text d-md-flex pt-4">
            <div class="pr-4 pb-4">
              <a href="https://vueschool.io/privacy" style="color: white; text-decoration: none">Privacy Policy</a>
            </div>
            <div class="pr-4 pb-4">
              <a href="https://vueschool.io/terms" style="color: white; text-decoration: none">Terms & Conditions</a>
            </div>
            <div class="pr-4 pb-4">
              <a href="https://vueschool.io/contact" style="color: white; text-decoration: none">Contact Us</a>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import CustomInput from "vue2-custom-input";

export default {
    components: {
        CustomInput
    }
}
</script>