<script lang="ts" setup>
import { ref } from "vue";
import angry from "../../feeling_imgs/angry.png";
import cute from "../../feeling_imgs/cute.png";
import excited from "../../feeling_imgs/excited.png";
import pain from "../../feeling_imgs/pain.png";
import shocked from "../../feeling_imgs/shocked.png";
import smile from "../../feeling_imgs/smile.png";
const result = ref("");
const OnClick = (name: string) => {
  result.value = name;
};
</script>

<template>
  <v-container>
    <v-row>
      <v-col>
        <v-img :src="angry" v-if="result === 'ANGRY'"></v-img>
        <v-img :src="cute" v-if="result === 'CUTE'"></v-img>
        <v-img :src="excited" v-if="result === 'EXCITED'"></v-img>
        <v-img :src="pain" v-if="result === 'PAIN'"></v-img>
        <v-img :src="shocked" v-if="result === 'SHOCKED'"></v-img>
        <v-img :src="smile" v-if="result === 'SMILE'"></v-img>
      </v-col>
      <v-col lass="d-flex flex-column mb-6">
        <p class="text-h2 text-center mt-5 mb-5">{{ result }}</p>
        <v-btn
          :class="'mb-4'"
          width="100%"
          @click="OnClick('ANGRY')"
          :color="result == 'ANGRY' ? 'yellow' : 'undefined'"
          >ANGRY</v-btn
        >
        <v-btn
          :class="'mb-4'"
          width="100%"
          @click="OnClick('CUTE')"
          :color="result == 'CUTE' ? 'yellow' : 'undefined'"
          >CUTE</v-btn
        >
        <v-btn
          :class="'mb-4'"
          width="100%"
          @click="OnClick('EXCITED')"
          :color="result == 'EXCITED' ? 'yellow' : 'undefined'"
          >EXCITED</v-btn
        >
        <v-btn
          :class="'mb-4'"
          width="100%"
          @click="OnClick('PAIN')"
          :color="result == 'PAIN' ? 'yellow' : 'undefined'"
          >PAIN</v-btn
        >
        <v-btn
          :class="'mb-4'"
          width="100%"
          @click="OnClick('SHOCKED')"
          :color="result == 'SHOCKED' ? 'yellow' : 'undefined'"
          >SHOCKED</v-btn
        >
        <v-btn
          :class="'mb-4'"
          width="100%"
          @click="OnClick('SMILE')"
          :color="result == 'SMILE' ? 'yellow' : 'undefined'"
          >SMILE</v-btn
        >
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped></style>
