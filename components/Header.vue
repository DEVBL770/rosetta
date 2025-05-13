<template>
  <header class="bg-gray-700 text-white">
    <div class="max-w-screen-xl mx-auto flex justify-between items-center p-4">
      <!-- Logo -->
      <img src="https://static.wixstatic.com/media/a99bfb_51d08cb347e14efa80d703d7c8667eed~mv2.png/v1/fill/w_129,h_67,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/Logo%20Jacob%20nouveau%20Blanc.png" alt="Logo Jacob Meat Peaker" class="h-16" />

      <!-- Hamburger Icon -->
      <button class="lg:hidden text-white" @click="toggleMenu">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16"></path>
        </svg>
      </button>

      <!-- Menu Mobile -->
      <transition name="fade">
        <nav v-if="isMenuOpen" class="absolute top-0 left-0 w-full h-screen bg-[#4e5d82] z-40 flex flex-col items-center justify-center space-y-6 text-xl">
          <a v-for="item in menuItems" :key="item.id" :href="`#${item.id}`" class="hover:underline text-white font-serif" @click="closeMenu">
            {{ item.label }}
          </a>
        </nav>
      </transition>

      <!-- Desktop Menu -->
      <nav class="hidden lg:flex space-x-6">
        <a v-for="item in menuItems" :key="item.id" :href="`#${item.id}`" class="text-white hover:text-gray-300 font-serif">
          {{ item.label }}
        </a>
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

// Mise à jour des éléments du menu avec les nouvelles sections
const menuItems = [
  { id: 'burgers', label: 'Meat Burgers' },
  { id: 'chicken', label: 'Chicken' },
  { id: 'fish', label: 'Fish' },
  { id: 'signatures', label: 'Signatures' },
  { id: 'sides', label: 'Accompagnements' },
  { id: 'desserts', label: 'Desserts' },
  { id: 'boissons', label: 'Boissons' }
]
</script>

<style scoped>
/* Ajout de la police Playfair Display */
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&display=swap');

/* Application de la police */
body {
  font-family: 'Playfair Display', serif;
}

/* Animation pour le menu mobile */
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}

/* Amélioration du menu mobile */
nav a {
  transition: color 0.3s ease, text-decoration 0.3s ease;
}

/* Change de couleur au survol */
nav a:hover {
  color: #838383; /* Jaune doux */
  text-decoration: underline;
}

/* Menu Desktop : hover */
nav.desktop a:hover {
  color: #fffdf7;
  text-decoration: underline;
}
</style>
