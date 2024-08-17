<template>
  <div>
    <Head>
      <Title>Details for {{ product.title }}</Title>
    </Head>
    <ProductDetails :product="product" />

  </div>
</template>


<script setup>
  // get the id of the product
  const { id } = useRoute().params;

  // fetch the detail for the specified product
  const {data: product} = await useFetch(`https://fakestoreapi.com/products/${id}`, { key: id })
  
  if (!product.value) {
    throw createError({
      statusCode: 404,
      statusMessage: "Product not found!",
    })
  }

  // get the page layout
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