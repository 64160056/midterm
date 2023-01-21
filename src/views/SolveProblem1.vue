<script lang="ts" setup>
import { ref } from "vue";
import angry from "../../feeling_imgs/angry.png";
const result = ref("");
</script>

<template>
  <v-container>
    <v-row>
      <v-col>
        <v-img :src="angry"></v-img>
      </v-col>
      <v-col> </v-col>
    </v-row>
  </v-container>
</template>

<style scoped></style>
