<template>
    <div>
        <header class="hero-section" style="position: relative">
            <div class="d-flex justify-center justify-lg-space-between white--text pr-8">
                <div class="d-flex text-capitalize align-center mr-8 mr-md-16" style="height: 5rem ">
                    <div class="">
                        <a href="https://vueschool.io/">
                            <v-img 
                                src="../assets/vueschool_logo_multicolor_negative.svg" 
                                alt="vue school logo"
                            />
                        </a>
                    </div>
                    <div class="d-none d-md-flex align-center" style="height: 5rem">
                        <v-hover v-slot="{hover}">
                            <div class="pr-4" :class="{'on-hover': hover}">
                                <a 
                                    href="https://vueschool.io/courses" 
                                    class="white--text"
                                    style="text-decoration: none"
                                > 
                                    courses 
                                </a>
                            </div>
                        </v-hover>

                        <v-hover v-slot="{hover}">
                            <div class="pr-4" :class="{'on-hover': hover}">
                                <a 
                                    href="https://vueschool.io/workshops" 
                                    class="white--text"
                                    style="text-decoration: none"
                                >
                                    workshops
                                </a>
                            </div>
                        </v-hover>

                        <v-hover v-slot="{hover}">
                            <div class="pr-4" :class="{'on-hover': hover}">
                                <a 
                                    href="https://vueschool.io/the-vuejs-master-class/" 
                                    class="white--text"
                                    style="text-decoration: none"
                                >
                                    Masterclass
                                </a>
                            </div>
                        </v-hover>

                        <v-hover v-slot="{hover}">
                            <div class="pr-4" :class="{'on-hover': hover}">
                                <a 
                                    href="https://vueschool.io/plans" 
                                    class="white--text"
                                    style="text-decoration: none"
                                >
                                    Plans
                                </a>
                            </div>
                        </v-hover>
                    </div>
                    </div>

                    <div class="d-flex align-center text-capitalize" style="height: 5rem">
                    <div class="pr-4">
                        <v-icon class="white--text">mdi-magnify</v-icon>
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
                        <v-hover v-slot="{hover}">
                            <div class="pr-4" :class="{'on-hover': hover}">
                                <a 
                                    href="https://vueschool.io/login"
                                    style="text-decoration: none"
                                    class="white--text"
                                >
                                    login
                                </a>
                            </div>
                        </v-hover>

                        <v-hover v-slot="{hover}">
                            <div class="pr-4" :class="{'on-hover': hover}">
                                <a 
                                    href="https://vueschool.io/register"
                                    style="text-decoration: none"
                                    class="white--text"
                                >
                                    create account
                                </a>
                            </div>
                        </v-hover>
                        
                    </div>
                </div>
            </div>

            <div class="d-flex align-center white--text px-6 mt-8">
                <div>
                    <div
                        class="text-h4 text-md-h3 font-weight-regular py-8 caption"
                        style="max-width: 70rem; width: 90%; letter-spacing: 1.09px;"
                    >
                        Learn Vue.js and modern, cutting-edge front-end technologies from core-team members and industry experts with our premium tutorials and video courses
                    </div>
                    <div class="pb-4 font-weight-regular">Join our Vue.js community to get started:</div>
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
                                class="white--text text-body-1 text-sm-h5 mr-2 py-4 py-sm-6 px-4 px-sm-8 font-bold"
                            >
                                Start learning
                            </v-btn>
                        </div>
                    </div>
                </div>
            </div>

            <a 
                href="#courses" 
                style="position: absolute; bottom: 0; left: 50%; text-decoration: none"
            >
                <v-icon 
                    large
                    style="cursor: pointer"
                    color="white"
                >
                    mdi-menu-down
                </v-icon>
            </a>
      
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

  .caption {
    line-height: 4.5rem !important;
  }

@media all and (max-width: 37.25em) {
    .caption {
        line-height: 4rem !important;
    }
}

</style>