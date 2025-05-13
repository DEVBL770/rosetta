<template>
  <header class="bg-gray-900 text-white">
    <div class="max-w-screen-xl mx-auto flex justify-between items-center p-4">
      <img src="https://static.wixstatic.com/media/a99bfb_51d08cb347e14efa80d703d7c8667eed~mv2.png/v1/fill/w_129,h_67,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/Logo%20Jacob%20nouveau%20Blanc.png" alt="Logo Jacob Meat Peaker" class="h-16" />

      <!-- Hamburger Icon -->
      <button class="lg:hidden text-white" @click="toggleMenu">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16"></path>
        </svg>
      </button>

      <!-- Menu Mobile -->
      <nav v-if="isMenuOpen" class="absolute top-16 right-4 bg-gray-800 text-white p-4 rounded-lg lg:hidden">
        <ul>
          <li><a href="#burgers" class="block py-2 px-4 hover:bg-gray-700" @click="closeMenu">Burgers</a></li>
          <li><a href="#chicken" class="block py-2 px-4 hover:bg-gray-700" @click="closeMenu">Poulet</a></li>
          <li><a href="#fish" class="block py-2 px-4 hover:bg-gray-700" @click="closeMenu">Poisson</a></li>
        </ul>
      </nav>

      <!-- Desktop Menu -->
      <nav class="hidden lg:flex space-x-6">
        <a href="#burgers" class="text-white hover:text-gray-300">Burgers</a>
        <a href="#chicken" class="text-white hover:text-gray-300">Poulet</a>
        <a href="#fish" class="text-white hover:text-gray-300">Poisson</a>
      </nav>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
  isMenuOpen.value = false
}
</script>
