<script setup lang="ts"></script>

<template>
  <header class="py-4 border-b bg-white shadow-md">
    <nav class="flex container items-center justify-between">
      <NuxtLink to="/" class="flex gap-2 items-center">
        <NuxtImg width="56px" src="/icon-green.png" format="webp" alt="Nuxtcipes Logo" />
        <span class="text-3xl font-bold text-green-600">Nuxtcipes</span>
      </NuxtLink>
      <ul class="flex items-center gap-6 text-xl font-semibold capitalize">
        <li>
          <NuxtLink to="/" class="hover:text-green-600 transition-colors duration-300">Home</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about" class="hover:text-green-600 transition-colors duration-300">About</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/recipes" class="hover:text-green-600 transition-colors duration-300">Recipes</NuxtLink>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
header {
  position: sticky;
  top: 0;
  z-index: 1000;
}
</style>
