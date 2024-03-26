<template>
  <div>
    <p>
      {{ product.title }} and the id is <b>{{ product.id }}</b>
    </p>
    <span>{{ product.price }}</span>
    <p>
      {{ product.description }}
    </p>
  </div>
</template>

<script setup>
const { id } = useRoute().params;

const url = "https://fakestoreapi.com/products/" + id;

const { data: product } = await useFetch(url);

definePageMeta({
  layout: "products",
});
</script>
