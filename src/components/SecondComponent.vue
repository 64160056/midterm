<script setup lang="ts">
import { useCounterStore } from "@/stores/counter";
const Counter = useCounterStore();
</script>
<template>
  <v-card-text class="text-h7" width="250px" height="150px"
    >Second Component</v-card-text
  >
  <v-card-text>{{ Counter.doubleCount }}</v-card-text>
  <v-btn @click="Counter.decrease">DECREASE</v-btn>
</template>
