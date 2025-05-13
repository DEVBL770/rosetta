<template>
  <header class="flex justify-between items-center px-6 py-4 shadow-md bg-white fixed w-full z-50">
    <div class="flex items-center space-x-4">
      <img src="https://static.wixstatic.com/media/a99bfb_9c7e97010cbb487ea470ca08921507d7~mv2.png/v1/fill/w_146,h_85,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/image001%20(2)_edited.png" alt="Logo" class="h-10" />
    </div>
    <nav class="hidden md:flex space-x-6 text-lg">
      <a href="#burgers" class="hover:text-primary transition">Burgers</a>
      <a href="#chicken" class="hover:text-primary transition">Chicken</a>
      <a href="#fish" class="hover:text-primary transition">Fish</a>
    </nav>
    <!-- Hamburger Menu -->
    <div class="md:hidden">
      <button @click="toggleMenu" class="focus:outline-none">
        <svg v-if="!isOpen" xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
      <transition name="fade">
        <div v-if="isOpen" class="absolute top-20 right-6 bg-white shadow-lg rounded-lg py-4 px-6 space-y-4">
          <a href="#burgers" class="block" @click="toggleMenu">Burgers</a>
          <a href="#chicken" class="block" @click="toggleMenu">Chicken</a>
          <a href="#fish" class="block" @click="toggleMenu">Fish</a>
        </div>
      </transition>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'
const isOpen = ref(false)
const toggleMenu = () => {
  isOpen.value = !isOpen.value
}
</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.3s ease;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
</style>
