<script lang="ts" setup>
import { ref } from "vue";
import angry from "../../feeling_imgs/angry.png";
import cute from "../../feeling_imgs/cute.png";
import excited from "../../feeling_imgs/excited.png";
import pain from "../../feeling_imgs/pain.png";
import shocked from "../../feeling_imgs/shocked.png";
import smile from "../../feeling_imgs/smile.png";
const result = ref("");
</script>

<template>
  <v-container>
    <v-row>
      <v-col>
        <v-img :src="angry"></v-img>
        <v-img :src="cute"></v-img>
        <v-img :src="excited"></v-img>
        <v-img :src="pain"></v-img>
        <v-img :src="shocked"></v-img>
        <v-img :src="smile"></v-img>
      </v-col>
      <v-col>
        <v-btn :class="'mb-4'" width="100%">ANGRY</v-btn>
        <v-btn :class="'mb-4'" width="100%">CUTE</v-btn>
        <v-btn :class="'mb-4'" width="100%">EXCITED</v-btn>
        <v-btn :class="'mb-4'" width="100%">PAIN</v-btn>
        <v-btn :class="'mb-4'" width="100%">SHOCKED</v-btn>
        <v-btn :class="'mb-4'" width="100%">SMILE</v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped></style>
