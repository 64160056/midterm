<script setup lang="ts">
import { useCounterStore } from "@/stores/counter";
const Counter = useCounterStore();
</script>
<template>
  <v-card-text class="text-h7" width="250px" height="150px">First Component</v-card-text>
  <v-card-text >{{ Counter.count }}</v-card-text>
  <v-btn @click="Counter.increment">INCREMENT</v-btn>
</template>
