<script setup lang="ts">
</script>

<template>
  <main>
    <section class="container py-20 px-4 md:px-20 bg-gray-100 rounded-lg shadow-lg">
      <h1 class="text-6xl font-extrabold mb-6 text-center text-balance text-gray-800">About Nuxtcipes:</h1>
      <p class="text-xl font-extrabold mb-6 text-center text-balance max-w-screen-lg mx-auto text-gray-700">
        Nuxtcipes is a recipe application based on the dummyJSON API, created by John Komarnicki for
        the <span class="font-bold text-gray-900">Build Modern Apps with Nuxt</span> course.
      </p>
      <p class="text-lg mb-4 text-justify max-w-screen-md mx-auto text-gray-600">
        Our mission is to provide a platform where users can discover, create, and share their favorite recipes. 
        Whether you are a professional chef or a home cook, Nuxtcipes has something for everyone.
      </p>
      <p class="text-lg mb-4 text-justify max-w-screen-md mx-auto text-gray-600">
        We offer a wide variety of recipes from different cuisines, and our easy-to-use interface makes it simple 
        to find the perfect recipe for any occasion. Join our community and start cooking today!
      </p>
      <h2 class="text-4xl font-bold mb-4 text-center text-gray-800">Features:</h2>
      <ul class="list-disc list-inside text-lg mb-4 max-w-screen-md mx-auto text-gray-600">
        <li class="mb-2">Discover new recipes from around the world</li>
        <li class="mb-2">Create and share your own recipes</li>
        <li class="mb-2">Save your favorite recipes for easy access</li>
        <li class="mb-2">Search for recipes by ingredients, cuisine, and more</li>
      </ul>
      <h2 class="text-4xl font-bold mb-4 text-center text-gray-800">Contact Us:</h2>
      <p class="text-lg mb-4 text-center text-gray-600">
        If you have any questions or feedback, feel free to reach out to us at 
        <a href="mailto:support@nuxtcipes.com" class="text-blue-500 underline">support@nuxtcipes.com</a>.
      </p>
      <div class="text-center">
        <NuxtLink to="/" class="text-blue-500 underline hover:text-blue-700">Back to Home</NuxtLink>
      </div>
    </section>
  </main>
</template>
