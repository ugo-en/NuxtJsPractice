<template>
  <div>
    <h2>Products details for {{ id }}</h2>
    
    <ProductDetails :product="product" />

  </div>
</template>


<script setup>
  const { id } = useRoute().params;

  // fetch the detail for the specified product
  const {data: product} = await useFetch(`https://fakestoreapi.com/products/${id}`, { key: id })
  
  definePageMeta({
      layout: "products-layout",
  })
</script>

<style scoped>
h2{
    color: blue;
}
p {
    word-wrap: break-word;
}
</style>