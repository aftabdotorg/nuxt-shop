<template>
  <div class="card text-center">
    <img
      class="image"
      :src="`${product.thumbnail}`"
      :alt="`${product.name}}`"
    />
    <p class="font-bold text-gray-500 m-4 truncate">{{ product.title }}</p>
    <NuxtLink :to="`/products/${product.id}`">
      <p class="bg-[#155e75] text-white px-3 py-2 rounded-md text-sm text-white my-4 justify-between">View Details</p>
    </NuxtLink>
  </div>
</template>

<script setup>
const { product } = defineProps({
  product: {
    type: Object,
    required: true,
  },
});
</script>

<style scoped>
.image {
  display: flex;
  justify-content: center;
  margin: auto;
  width: 240px;
  height: 140px;
  object-fit: contain;
}
</style>
