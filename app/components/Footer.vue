<template>
    <footer class="bg-gray-800 text-white py-5">
        <div class="container mx-auto flex justify-between items-center flex-wrap">
            <p>&copy; 2023 Your Company. All rights reserved.</p>
            <nav>
                <ul class="flex space-x-4">
                    <li><NuxtLink to="#about" class="hover:underline">About</NuxtLink></li>
                    <li><NuxtLink to="#services" class="hover:underline">Services</NuxtLink></li>
                    <li><NuxtLink to="#contact" class="hover:underline">Contact</NuxtLink></li>
                </ul>
            </nav>
        </div>
    </footer>
</template>

<script setup lang="ts">
</script>

<style scoped>
/* No additional styles needed */
</style>
