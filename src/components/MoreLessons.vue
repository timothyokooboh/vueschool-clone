<template>
    <div>
        <div
            class="py-16 px-4"
            style="background: #E6EDFC"
        >
        
            <div class="display-2 pb-8" style="color: #5E527F">Featured lessons</div>
            
            <div class="d-md-flex justify-space-between white d-lg-block">
                <div
                    v-for="(course, index) in featuredLessons"
                    :key="index"
                    class="py-4 px-8 rounded-t white"
                >
                    <div class="d-md-block d-lg-flex align-center">
                       <div>
                            <v-avatar tile class="rounded-lg course-image">
                            <v-img :src="course.image"></v-img>
                            </v-avatar>
                        </div>
                        
                        <div class="d-flex mt-4 flex-column flex-sm-row align-sm-center justify-center justify-sm-space-between" style="width: 100%">
                            <div class="order-2 order-sm-1">
                                <div class="pb-4 pl-sm-4">{{course.title}}</div>
                                <div class="d-flex align-center px-sm-4">
                                    <div class="pr-2">
                                    <img src="../assets/icon_play.svg" alt="play icon" class="pt-1">
                                    </div>
                                    <div class="h5 text-sm-h4">{{course.description}}</div>
                                </div>
                            </div>
                        </div>

                        <div class="order-1 order-sm-2 d-flex flex-wrap justify-space-between align-center d-sm-block mb-4">
                            <div class="d-flex align-center pb-sm-4">
                                <div class="pr-2">
                                <img src="../assets/icon_time.svg" alt="time icon" class="pt-1">
                                </div>
                                <div>{{course.duration}}</div>
                            </div>
                            <div class="text-uppercase title py-1 px-2 grey--text text--darken-2" style="background: #EEEDF2 ">
                                {{course.difficulty}}
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="display-2 pt-16 pb-8" style="color: #5E527F">Latest lessons</div>
            <div class="d-md-flex justify-space-between white d-lg-block">
                <div
                    v-for="(course, index) in latestLessons"
                    :key="index"
                    class="py-4 px-8 rounded-t white"
                >
                    <div class="d-md-block d-lg-flex align-center">
                        <div>
                            <v-avatar tile class="rounded-lg course-image">
                            <v-img :src="course.image"></v-img>
                            </v-avatar>
                        </div>
                        
                        <div class="d-flex mt-4 flex-column flex-sm-row align-sm-center justify-center justify-sm-space-between" style="width: 100%">
                            <div class="order-2 order-sm-1">
                                <div class="pb-4 pl-sm-4">{{course.title}}</div>
                                <div class="d-flex align-center px-sm-4">
                                    <div class="pr-2">
                                        <img src="../assets/icon_play.svg" alt="play icon" class="pt-1">
                                    </div>
                                    <div class="h5 text-sm-h4">{{course.description}}</div>
                                </div>
                            </div>

                            <div class="order-1 order-sm-2 d-flex flex-wrap justify-space-between align-center d-sm-block mb-4">
                                <div class="d-flex align-center pb-sm-4">
                                    <div class="pr-2">
                                        <img src="../assets/icon_time.svg" alt="time icon" class="pt-1">
                                    </div>
                                    <div>{{course.duration}}</div>
                                </div>
                                <div class="text-uppercase title py-1 px-2 grey--text text--darken-2" style="background: #EEEDF2 ">
                                    {{course.difficulty}}
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
    
            <div class="display-2 pt-16 pb-8" style="color: #5E527F">Upcoming lessons</div>
            <div class="d-md-flex justify-space-between white d-lg-block">
                <div
                    v-for="(course, index) in upcomingLessons"
                    :key="index"
                    class="py-4 px-8 rounded-t white"
                >
                    <div class="d-md-block d-lg-flex align-center">
                        <div 
                            class="course-image rounded-lg text-uppercase d-flex align-center justify-center "
                            style="background-color: #3D377A"
                        >
                            <div class="display-2 white--text">
                                {{course.image}}
                            </div>
                        </div>

                        <div class="d-flex mt-4 flex-column flex-sm-row align-sm-center justify-center justify-sm-space-between" style="width: 100%">
                            <div class="order-2 order-sm-1">
                                <div class="pb-4 pl-sm-4">{{course.title}}</div>
                                <div class="d-flex align-center px-sm-4">
                                    <div class="pr-2">
                                        <img src="../assets/icon_play.svg" alt="play icon" class="pt-1">
                                    </div>
                                    <div class="h5 text-sm-h4">{{course.description}}</div>
                                </div>
                            </div>
                        </div>


                        <div class="order-1 order-sm-2 d-flex flex-wrap justify-space-between align-center d-sm-block mb-4">
                            <div class="text-uppercase title py-1 px-2 grey--text text--darken-2" style="background: #EEEDF2 ">
                                {{course.difficulty}}
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="text-center mt-8">
                <v-btn color="#4DC3A0" class="rounded-pill py-6 py-sm-8 px-8 px-sm-12 title text-sm-h4 white--text mb-4">browse lessons</v-btn>
            </div>
        </div>
    </div>
</template>

<script>
import featuredLessons from "../featuredLessons";
import latestLessons from "../latestLessons";
import upcomingLessons from "../upcomingLessons";

export default {
    data() {
        return {
            featuredLessons,
            latestLessons,
            upcomingLessons
        }
    }
}
</script>

<style scoped>
  .course-image {
    height: 130px !important;
    width: 250px !important;
  }

   @media all and (max-width: 768px ) {
    .course-image {
      width: 100% !important;
    }
  } 
</style>