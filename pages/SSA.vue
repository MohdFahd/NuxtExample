<template>
  <div>
    <p>{{ pageType }} page</p>
    <pre>Time after hydration: {{ new Date().toUTCString() }} </pre>
    <pre>Time in server rendered HTML: {{ data }}</pre>
    <NuxtLink to="/">Home</NuxtLink>
  </div>
</template>
<script setup>
const pageType = "SPA"; // value differs for each route
const { data } = await useFetch("https://fakestoreapi.com/products");
</script>
