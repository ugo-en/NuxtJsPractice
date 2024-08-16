<template>
    <div>
      <div class="grid grid-cols-4 gap-5">
        <div v-for="p in products">
          <ProductCard :product="p" />
        </div>
      </div>
    </div>
  </template>
  
<script setup>
  definePageMeta({
      layout: "products-layout",
  })

  // fetch products
  const { data: products } = await useFetch("https://fakestoreapi.com/products")
</script>
  
<style scoped>
  h2{
      color: green;
  }
  p {
      word-wrap: break-word;
  }
</style>