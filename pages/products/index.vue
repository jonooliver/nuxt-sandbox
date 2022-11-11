<template>
  <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-3 lg:gap-5">
    <div v-for="product in products">
      <ProductCard :product="product" />
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "products",
});

const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<style scoped></style>
