<template>
  <div>
    <h2>Products details for {{ id }}</h2>
    <br>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Labore saepe recusandae vitae magnam impedit quibusdam at veniam dolores quisquam, vel sit beatae, tempora, nihil tenetur inventore pariatur neque consectetur dignissimos?</p>
    <br>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Labore saepe recusandae vitae magnam impedit quibusdam at veniam dolores quisquam, vel sit beatae, tempora, nihil tenetur inventore pariatur neque consectetur dignissimos?</p>
  </div>
</template>


<script setup>
  const { id } = useRoute().params;
  
  definePageMeta({
      layout: "products",
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