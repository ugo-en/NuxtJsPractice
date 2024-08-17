<template>
    <div class="card">
        <div class="grid md:grid-cols-2 sm:grid-cols-1 gap-10">
            <div class="md:p-7 sm:p-2">
                <img :src="product.image" alt="product image" class="mx-auto my-7">
            </div>
            <div class="md:p-7 sm:p-2">
                <h2 class="font-bold text-4xl my-7">{{ product.title }}</h2>
                <p class="text-xl my-7">Price - £{{ price_in_gbp }} | ${{ price_in_usd }}</p>
                <h3 class="font-bold border-b-2 mb-4 pb-2">Product Description:</h3>
                <p class="mb-7 word-wrap">{{ product.description }}</p>
                <button class="btn flex">
                    <i class="material-icons mr-2">add_shopping_cart</i>
                    <span>Add to Cart</span>
                </button>
            </div>
        </div>
    </div>
</template>

<script setup>
    // get product details
    const { product } = defineProps(["product"])

    // get conversion in pounds
    const { data } = await useFetch("/api/currency/GBP")
    const gbp_value = data.value.GBP.value

    // price in USD will be the default product price
    const price_in_usd = product.price.toFixed(2)

    // convert it to GBP
    let price_in_gbp = price_in_usd * gbp_value
    price_in_gbp = price_in_gbp.toFixed(2)
</script>

<style scoped>
    img {
        max-width: 400px;
    }
</style>