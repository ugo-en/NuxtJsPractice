<template>
    <div>
      <header>
        <nav>
          <ul>
            <NuxtLink to="/">Merch</NuxtLink>
          </ul>
        </nav>
      </header>
    </div>

    <div>
        <slot />
    </div>

    <footer>
        <nav>
            <ul>
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
