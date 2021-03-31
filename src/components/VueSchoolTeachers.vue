<template>
    <div>
        <div 
        class="pb-16"
        style="background-color: #EDF3FF"
      >
        <div 
          class="text-center display-2 py-16"
          style="color: #5E527F"
        >
          Our teachers are industry experts
        </div>
      </div>

      <div 
        style="background-color: #4E47AA"
        class="py-16 d"
      >
        <div
          style="background-color: #4E47AA" 
          class="d-flex flex-wrap align-center justify-center"
        >
          <v-card
            v-for="teacher in teachers"
            :key="teacher"
            max-width="40rem"
            width="90%"
            class="mr-2 mb-16"
            style="position: relative; bottom: 10rem"
          >
            <div class="text-center">
              <v-avatar 
                size="100"
                style="position: relative; bottom: 5rem"
              >
                <v-img 
                  :src="teacher.image"
                  class="rounded-circle"
                  style="border: 7px solid white"
                >
                </v-img>
              </v-avatar>
            </div>
            <div 
              class="text-center text-capitalize display-1"
              style="position: relative; bottom: 2rem; color: #5E527F"
            > 
              {{teacher.name}}
            </div>
            <div
              v-for="(description, index) in teacher.descriptions"
              :key="index"
              class="pb-4 px-8 text-center"
              style="color: #5E527F"
            >
                {{description}}
            </div>
            <div class="d-flex align-center justify-center py-4">
              <div 
                style="background: #373187; height: 3.5rem; width: 3.5rem" 
                class="rounded-circle d-flex alihn-center justify-center mr-2"
              >
                <v-icon class="white--text">mdi-twitter</v-icon>
              </div>
              <div 
                style="background: #373187; height: 3.5rem; width: 3.5rem" 
                class="rounded-circle d-flex alihn-center justify-center mr-2"
              >
                <v-icon class="white--text">mdi-github</v-icon>
              </div>
            </div>
          </v-card>
        </div>
      
        <div 
          class="d-flex flex-column align-center justify-center"
          style="position: relative; bottom: 10rem"
        >
          <div class="d-flex flex-wrap px-4">
            <div>
              <v-avatar size="100">
                <v-img 
                  src="../assets/evan.jpg"
                  style="border: 7px solid white"
                >
                </v-img>
              </v-avatar>
            </div>
            <div class="d-flex align-center white--text ml-4">
              <div class="hidden-xs-only display-2 font-weight-bold mr-4 text-uppercase">
                patreon
              </div>
              <div
                class="white mr-4 hidden-xs-only"
                style="height: 7rem; width: 5px"
              >
              </div>
              <div>
                <div class="text-capitalize display-2 mt-4"> evan you</div>
                <div>Creator of Vue.js</div>
              </div>
            </div>
          </div>
          <div 
            class="white--text px-4 pt-4"
            style="max-width: 40rem"
          >
            Thanks to fine people like you, Vue School can proudly sponsor Evan and the future of Vue.js by being a Platinum Patreon.</div>
        </div>
      </div>
    </div>
</template>

<script>
import teachers from "../teachers";

export default {
    data() {
        return {
            teachers
        }
    }
}
</script>