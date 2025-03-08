<script setup lang="ts">
import { type Recipe } from "../../types/types";

defineProps<{
  recipe: Recipe;
}>();
</script>

<template>
  <div class="flex flex-col shadow-lg rounded-md overflow-hidden transition-transform transform hover:scale-105">
    <NuxtImg
      :src="recipe.image"
      sizes="xs:100vw sm:50vw lg:400px"
      format="webp"
      densities="x1"
      alt="Recipe Image"
      class="rounded-t-md object-cover h-48"
    />
    <div class="flex flex-col py-6 px-4 flex-1 bg-white">
      <p class="text-xl lg:text-2xl font-semibold mb-2">{{ recipe.name }}</p>
      <div class="font-normal w-full flex gap-8 text-lg lg:text-xl mb-4 mt-auto">
        <div class="flex items-center gap-1">
          <UIcon name="i-mdi-clock-time-eight-outline" class="text-dodgeroll-gold-500" />
          <span>{{ recipe.cookTimeMinutes }} mins</span>
        </div>
        <div class="flex items-center gap-1">
          <UIcon name="i-mdi-fire" class="text-dodgeroll-gold-500" />
          <span>{{ recipe.caloriesPerServing }} kcal</span>
        </div>
        <div class="flex items-center gap-1">
          <UIcon name="i-mdi-star" class="text-dodgeroll-gold-500" />
          <span>{{ recipe.rating }} ({{ recipe.reviewCount }})</span>
        </div>
      </div>
      <UButton
        :ui="{
          base: 'self-start',
        }"
        :to="`/recipes/${recipe.id}`"
        label="View"
        class="bg-blue-500 text-white py-2 px-4 rounded hover:bg-blue-600 transition-colors"
      />
    </div>
  </div>
</template>

<style scoped>
/* Add any additional styles here */
</style>
