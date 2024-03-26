<template>
  <div class="card text-center">
    <img :src="product.image" class="thump" alt="" />
    <h1 class="font-bold text-gray-600 my-3">{{ product.title }}</h1>
    <p class="truncate">{{ product.description }}</p>
    <h3 class="font-bold my-5">{{ product.price }}$</h3>
    <NuxtLink :to="`/products/${product.id}`" class="btn bg-blue-600"
      >View details</NuxtLink
    >
  </div>
</template>

<script setup>
const { product } = defineProps({
  product: {
    type: Object,
  },
});
</script>

<style scope>
.thump {
  max-width: 70%;
  max-height: 120;
  margin: 0% auto;
}
</style>
