<script setup lang="ts">
import FirstComponentVue from "@/components/FirstComponent.vue";
import SecondComponent from "@/components/SecondComponent.vue";
const n = 0;
const emit = defineEmits<{
  (e: "up", id: number): void;
  (e: "down", value: string): void;
}>();
</script>
<template>
  <v-container>
    <v-row>
      <v-col cols="6"> <FirstComponentVue :n="n" /> </v-col>
      <v-col cols="6"> <SecondComponent :n="n" /> </v-col>
    </v-row>
  </v-container>
</template>
