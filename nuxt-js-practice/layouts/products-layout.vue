<template>
    <div>
      <header class="shadow-sm bg-white mb-4">
        <nav class="container mx-auto p-4 flex justify-between">
          <ul>            
            <NuxtLink to="/" class="material-icons text-2xl font-bold">home</NuxtLink>
            &nbsp;
            <NuxtLink to="/products" class="font-bold text-2xl">Merch</NuxtLink>
          </ul>
        </nav>
      </header>
    </div>

    <div>
        <slot />
    </div>

    <footer>
        <nav class="container mx-auto p-4 flex justify-between">
            <ul class="flex gap-4">
            <li>
                <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/about">About</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/products">Products</NuxtLink>
            </li>
            </ul>
        </nav>
    </footer>
</template>

<style>
  .router-link-exact-active {
      color: aquamarine;
  }
</style>
