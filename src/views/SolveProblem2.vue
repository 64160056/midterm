<script lang="ts" setup></script>

<template>
  <v-container>
    <v-row>
      <v-text-field
        label="Please input Number"
        :rules="[(v) => !!v || 'Number is not empty!!']"
      ></v-text-field>
    </v-row>
    <v-row>
      <v-col></v-col>
    </v-row>
  </v-container>
</template>
