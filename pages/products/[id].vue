<template>
  <section>
    <SingleProduct :product="data" />
  </section>
</template>

<script setup>
import { useRoute } from "vue-router";
const route = useRoute();
const id = route.params.id;
const URI = `https://dummyjson.com/products/${id}`;

// singular fetch

const { data } = await useFetch(URI, { key: id });

definePageMeta({
  layout: "default",
});
</script>

<style scoped></style>
