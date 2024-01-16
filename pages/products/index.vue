<template>
  <div class="grid grid-cols-3 gap-5" v-if="data && data.products">
    <div v-for="product in data.products">
      <ProductCard :product="product" />
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "default",
});

// label data as products after fetching
const { data } = await useFetch("https://dummyjson.com/products");
</script>

<style scoped></style>
