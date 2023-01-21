<script lang="ts" setup>
import { ref } from "vue";
const num = ref<number>(0);
</script>

<template>
  <v-container>
    <v-row>
      <v-text-field
        v-model.number="num"
        label="Please input Number"
        class="font-weight-bold"
        type="input"
        :rules="[(v) => !!v || 'Number is not empty!!']"
      ></v-text-field>
    </v-row>
    <v-row>
      <v-col v-for="n in num" :key="n" cols="1">
        {{ n }}
      </v-col>
    </v-row>
  </v-container>
</template>
