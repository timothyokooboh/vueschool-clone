<template>
    <div>
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
            <a 
                href="https://vueschool.io/courses" 
                style="text-decoration: none; color: #F63F75"
            >
                new content added weekly
            </a>
          </v-btn>
        </div>

        <div class="d-flex flex-wrap justify-center ml-3">
          <v-card
            v-for="course in courses"
            :key="course.title"
            class="mr-3 mb-8 rounded-lg"
            max-width="400"
            width="90%"
            style="position: relative;"
          >
           
            <v-avatar 
            tile 
            width="100%" 
            height="200"
            style="position: relative;"
            class="rounded-t-lg"
            >
             <v-hover v-slot="{hover}">
                <v-img 
                    :src="course.image"
                    :class="{'on-hover': hover}"
                >
                </v-img>
             </v-hover>
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
                    src="../assets/runtime.png" 
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
          <v-btn 
            color="#4DC3A0" 
            class="rounded-pill py-6 py-sm-8 px-8 px-sm-12 title text-sm-h4 white--text mb-4"
            >
                <a 
                    href="https://vueschool.io/courses"
                    class="white--text"
                    style="text-decoration: none"
                >
                    see all our courses
                </a>
            </v-btn>
          <div>
            <span style="color: #F63F75">Learn Vue.js</span> <span class="font-weight-bold grey--text text--darken-2 ">for $25/month or $190/year</span>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import courses from "../courses";

export default {
    data() {
        return {
            courses
        }
    }
}
</script>

<style scoped>
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

    .on-hover {
        transform: scale(1.1);
        transition: all .2s;
    }
</style>