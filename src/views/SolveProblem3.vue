<script lang="ts" setup>
import { ref } from "vue";

const products = ref(
  Array.from(Array(100).keys()).map((item) => {
    return {
      id: item,
      name: "Product " + (item + 1),
      price: (Math.floor(Math.random() * 100) + 1) * 10,
    };
  })
);
</script>
<template>
  <v-row>
    <v-col>
      <v-card class="v-col-4 ma-5">
        <v-card-title></v-card-title>
      </v-card>
    </v-col>
    <v-col>
      <v-table>
        <thead>
          <tr>
            <th class="text-left">id</th>
            <th class="text-left">name</th>
            <th class="text-left">price</th>
          </tr>
        </thead>
        <tbody>
          <td colspan="4">
            <p class="text-center font-weight-bold">NO Data</p>
          </td>
        </tbody>
      </v-table>

      <v-contianer>
        <p class="font-weight-bold text-h2">Sum:</p>
      </v-contianer>
    </v-col>
  </v-row>
</template>
