<template>
    <div>
        <header class="hero-section">
            <div class="d-flex justify-center justify-lg-space-between white--text">
                <div class="d-flex text-capitalize align-center mr-8 mr-md-16" style="height: 5rem ">
                    <div class="">
                        <v-img 
                        src="../assets/vueschool_logo_multicolor_negative.svg" 
                        alt="vue school logo"
                        />
                    </div>
                    <div class="d-none d-md-flex align-center" style="height: 5rem">
                        <div class="pr-4" >courses</div>
                        <div class="pr-4" >workshops</div>
                        <div class="pr-4" >masterclass</div>
                        <div>plans</div>
                    </div>
                    </div>

                    <div class="d-flex align-center text-capitalize" style="height: 5rem">
                    <div class="pr-4">
                        <v-icon>mdi-magnify</v-icon>
                    </div>
                    <div>
                        <v-icon 
                        class="hidden-md-and-up white--text"
                        @click="showMenu = true"
                        v-if="!showMenu"
                        >
                        mdi-dots-horizontal
                        </v-icon>
                        <v-icon
                        class="hidden-md-and-up white--text"
                        @click="showMenu = false"
                        v-if="showMenu"
                        >
                        mdi-close
                        </v-icon>
                    </div>
                    <div class="d-none d-md-flex align-center" style="height: 5rem">
                        <div class="pr-4">login</div>
                        <div class="pr-4">create account</div>
                    </div>
                </div>
            </div>

            <div 
                class="d-flex align-center white--text px-6"
                style="height: 60vh"
            >
                <div>
                    <div 
                        class="display-1 py-8"
                        style="max-width: 70rem; width: 90%; letter-spacing: 1.09px; line-height: 4.5rem"
                    >
                        Learn Vue.js and modern, cutting-edge front-end technologies from core-team members and industry experts with our premium tutorials and video courses</div>
                    <div class="pb-4">Join our Vue.js community to get started:</div>
                    <div class="white d-flex align-center">
                        <custom-input
                            placeholder="Your email"
                            color="white"
                            class="white"
                        >
                        </custom-input>
                        <div>
                            <v-btn 
                                color="#3DAD8B"
                                class="white--text headline mr-2 py-6 px-8 font-bold"
                            >
                                start learning
                            </v-btn>
                        </div>
                    </div>
                </div>
            </div>
        </header>

      <div 
        v-if="showMenu"
        class="hidden-md-and-up white--text pl-6 pt-4"
        style="background:#1B0742; position: absolute; top: 60px; left: 0; width: 100%; min-height: 100vh"
      >
        <v-hover v-slot="{hover}">
          <div 
            class="text-capitalize"
            :class="{'on-hover': hover}"
          >
            courses
          </div>
        </v-hover>
        <v-hover v-slot="{hover}">
          <div 
            class="text-capitalize pt-4"
            :class="{'on-hover': hover}"
          >
            workshops
          </div>
        </v-hover>
        <v-hover v-slot="{hover}">
          <div 
            class="text-capitalize pt-4"
            :class="{'on-hover': hover}"
          >
            master
          </div>
        </v-hover>
        <v-hover v-slot="{hover}">
          <div 
            class="text-capitalize pt-4"
            :class="{'on-hover': hover}"
          >
            plans
          </div>
        </v-hover>
        <v-hover v-slot="{hover}">
          <div 
            class="text-capitalize pt-4"
            :class="{'on-hover': hover}"
          >
            login
          </div>
        </v-hover>
        <v-hover v-slot="{hover}">
          <div 
            class="text-capitalize pt-4"
            :class="{'on-hover': hover}"
          >
            create account
          </div>
        </v-hover>
      </div>
    </div>
</template>

<script>
import CustomInput from "vue2-custom-input";

export default {
    name: "HeroSection",

    components: {
        CustomInput
    },
    
    data: () => ({
        showMenu: false
    }),
}
</script>

<style scoped>
.hero-section {
    background-image: url("../assets/hero-image.jpg");
    background-size: cover;
    /*background-position: center;*/
    min-height: 100vh;
  }

  .on-hover {
    border-bottom: 1px purple solid;
    cursor: pointer;
  }
</style>