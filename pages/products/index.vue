<template>
  <p>Products</p>

  <div class="grid grid-cols-4 gap-4">
    <div v-for="product in products" :key="product.id">
      <NuxtLink :to="`/products/${product.id}`">{{ product.title }}</NuxtLink>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "products",
});
const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<style></style>
