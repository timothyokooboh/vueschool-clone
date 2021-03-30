<template>
    <div>
        <header class="hero-section d-flex justify-center justify-lg-space-between white--text">
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
export default {
    name: "HeroSection",
    data: () => ({
        showMenu: false
    }),
}
</script>

<style scoped>
.hero-section {
    background-image: url("../assets/hero-image.jpg");
    background-size: cover;
    background-position: center;
    min-height: 100vh;
  }

  .on-hover {
    border-bottom: 1px purple solid;
    cursor: pointer;
  }
</style>