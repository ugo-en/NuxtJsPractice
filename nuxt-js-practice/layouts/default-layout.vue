<template>
    <div>
      <header class="shadow-sm bg-white mb-4">
        <nav class="container mx-auto p-4 flex justify-between">
          <NuxtLink to="/" class="font-bold">Nuxt Demo</NuxtLink>
          <ul class="flex gap-4">
            <li>
              <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/about">About</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/products" class="btn">Products</NuxtLink>
            </li>
          </ul>
        </nav>
      </header>
    </div>

    <div class="container mx-auto p-4">
        <slot />
    </div>
</template>

<style>
.router-link-exact-active {
    color: aquamarine;
}
</style>