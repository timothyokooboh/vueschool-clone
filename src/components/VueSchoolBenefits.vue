<template>
    <div>
        <div style="background-color: #3B348E" >
        <div class="d-flex flex-wrap justify-center white px-8">
          <div
            v-for="benefit in benefits"
            :key="benefit.title"
            class="py-8 text-center mr-8"
            style="max-width: 35rem; width: 90%"
          >
            <v-avatar size="100">
              <v-img :src="benefit.image"></v-img>
            </v-avatar>
            <div class="display-1 py-4">{{benefit.title}}</div>
            <div
              v-for="(description, index) in benefit.descriptions"
              :key="index"
              class="pb-4"
            >
              {{description}}
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import benefits from "../benefits";

export default {
    data() {
        return {
            benefits
        }
    }
}
</script>