<template>
  <p class="font-bold text-2xl my-2">Products</p>

  <div class="grid grid-cols-4 gap-4">
    <div v-for="product in products" :key="product.id">
      <productCard :product="product" />
    </div>
  </div>
</template>

<script setup>
// definePageMeta({
//   layout: "products",
// });
const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<!-- <style scope>
.router-link-exact-active {
  color: white;
}
</style> -->
