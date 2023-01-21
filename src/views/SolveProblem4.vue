<script setup lang="ts">
import FirstComponentVue from "@/components/FirstComponent.vue";
import SecondComponent from "@/components/SecondComponent.vue";
</script>
<template>
  <v-container>
    <v-row>
      <v-col> <FirstComponentVue /> </v-col>
      <v-col> <SecondComponent /> </v-col>
    </v-row>
  </v-container>
</template>
