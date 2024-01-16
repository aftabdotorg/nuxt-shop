<template>
  <div>Product ID : {{ id }}</div>
</template>

<script setup>
import { useRoute } from "vue-router";
const route = useRoute();
const id = route.params.id;

definePageMeta({
  layout: "products",
});
</script>

<style scoped></style>
