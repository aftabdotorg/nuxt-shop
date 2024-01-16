
import type { setBlockTracking } from 'vue';
<template>
  <div class="card">
    <section class="grid grid-cols-2 gap-10">
      <div class="p-7">
        <img
          :src="`${product.thumbnail}`"
          :alt="`${product.title}`"
          class="mx-auto my-7"
        />
      </div>
      <div class="p-7">
        <h2 class="text-4xl my-7">{{ product.title }}</h2>
        <p class="text-xl my-7">Price: ${{ product.price }}</p>
        <h2 class="font-bold border-b-2 mb-4 pb-2">Product Description</h2>
        <p class="mb-7">{{ product.description }}</p>
      </div>
    </section>
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

</style>
