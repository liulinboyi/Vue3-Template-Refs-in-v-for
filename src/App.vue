<script setup lang="ts">
import Product from './components/Product.vue';
import { ref } from 'vue';

let products = ref([]);

let items = ['abc', 'def'];

const show = () => {
  products.value.forEach((product: any) => {
    console.log(product.externalId);
  });
};
</script>

<template>
  <Product
    v-for="item in items"
    :externalId="item"
    :key="item"
    ref="products"
  />

  <button @click="show">Test</button>
</template>
