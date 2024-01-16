<template>
  <div>
    <header>
      <nav>
        <NuxtLink to="/products">Nuxt Products</NuxtLink>
      </nav>
    </header>

    <div>
      <slot />
    </div>
  </div>

  <footer>
    <ul>
      <li><NuxtLink to="/">Home</NuxtLink></li>
      <li><NuxtLink to="/products">Products</NuxtLink></li>
      <li><NuxtLink to="/about">About</NuxtLink></li>
    </ul>
  </footer>
</template>

<style scoped>
.router-link-exact-active {
  color: darkolivegreen;
}
</style>
