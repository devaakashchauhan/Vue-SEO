<script setup lang="ts">
import type { RecipeResponse   } from "~~/types/types";
import { ref } from "vue";

const { data, error } = await useFetch<RecipeResponse>(
  "https://dummyjson.com/recipes?limit=12"
);

const recipes = ref(data?.value?.recipes || []);

useSeoMeta({
  title: "Nuxtcipes",
  description: "Recipes for you to cook!",
  ogTitle: "Nuxtcipes",
  ogDescription: "Recipes for you to cook!",
  ogImage: "/nuxt-course-hero.png",
  ogUrl: `http://localhost:3000`,
  twitterTitle: "Nuxtcipes",
  twitterDescription: "Recipes for you to cook!",
  twitterImage: "/nuxt-course-hero.png",
  twitterCard: "summary",
});
</script>

<template>
  <section id="hero" class="py-20 bg-gradient-to-r from-indigo-500 to-purple-600 text-white text-center relative overflow-hidden">
    <img src="/nuxt-course-hero.png" alt="Hero Image" class="absolute inset-0 w-full h-full object-cover opacity-50">
    <div class="container mx-auto relative z-10">
      <h1 class="text-4xl lg:text-6xl font-bold mb-4">Welcome to Nuxtcipes</h1>
      <p class="text-lg lg:text-2xl mb-8">Discover, Create, and Share Amazing Recipes</p>
      <NuxtLink to="#recipes" class="bg-white text-blue-500 py-2 px-4 rounded hover:bg-gray-200">Explore Recipes</NuxtLink>
    </div>
  </section>

  <section id="recipes" class="py-20 container mx-auto bg-gradient-to-r from-gray-100 to-gray-200 rounded-lg p-8">
    <div class="text-center mb-12">
      <h2 class="text-3xl lg:text-5xl font-bold mb-2">Discover, Create, Share</h2>
      <p class="text-lg lg:text-xl text-gray-600">Check out our most popular recipes!</p>
    </div>
    <div v-if="!error" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-x-4 gap-y-8">
      <RecipeCard v-for="recipe in recipes" :key="recipe.id" :recipe="recipe" />
    </div>
    <p v-else class="text-xl text-center text-red-500">
      Oops, something went wrong. Please try again later.
    </p>
   
  </section>
</template>
