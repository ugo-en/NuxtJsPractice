<template>
    <div>
      <h2>About</h2>
      <br>
      <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Labore saepe recusandae vitae magnam impedit quibusdam at veniam dolores quisquam, vel sit beatae, tempora, nihil tenetur inventore pariatur neque consectetur dignissimos?</p>
      <br>
      <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Labore saepe recusandae vitae magnam impedit quibusdam at veniam dolores quisquam, vel sit beatae, tempora, nihil tenetur inventore pariatur neque consectetur dignissimos?</p>
    </div>
    <div>{{ data }}</div>
</template>
  
  
<script setup>    
    definePageMeta({
        layout: "default-layout",
    })
</script>
  
<style scoped>
    h2{
        color: yellow;
    }
    p {
        word-wrap: break-word;
    }
</style>