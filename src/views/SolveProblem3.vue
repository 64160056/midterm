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
interface Porps {
  id: number;
  name: string;
  price: number;
}
const sum = ref(0);
const selects = ref<Porps[]>([]);
const OnClick = (item: Porps) => {
  selects.value.push(item);
  sum.value = sum.value + item.price;
};
</script>
<template>
  <v-container>
    <v-row>
      <v-col class="flex-wrap d-flex overflow-auto h-screen justify-center">
        <v-card
          v-for="item of products"
          :key="item.id"
          class="v-col-3 ma-3 justify-center"
        >
          <v-card-title class="text-center">{{ item.name }}</v-card-title>
          <v-card-text class="text-center pa-0">{{ item.price }}</v-card-text>
          <v-card-actions class="justify-center">
            <v-btn @click="OnClick(item)">ADD</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>

      <v-col>
        <v-table height="600px">
          <thead>
            <tr>
              <th class="text-left">id</th>
              <th class="text-left">name</th>
              <th class="text-left">price</th>
            </tr>
          </thead>
          <tbody v-if="selects.length === 0">
            <td colspan="4">
              <p class="text-center font-weight-bold">NO Data</p>
            </td>
          </tbody>
          <tbody v-if="selects.length > 0">
            <tr v-for="(item, index) in selects" :key="index">
              <td>{{ item.id }}</td>
              <td>{{ item.name }}</td>
              <td>{{ item.price }}</td>
            </tr>
          </tbody>
        </v-table>

        <v-contianer>
          <p class="font-weight-bold text-h2">Sum: {{ sum }}</p>
        </v-contianer>
      </v-col>
    </v-row>
  </v-container>
</template>
