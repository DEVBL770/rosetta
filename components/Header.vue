<template>
  <header class="relative py-6 bg-transparent text-white">
    <div class="flex justify-between items-center max-w-5xl mx-auto px-4">
      <div class="text-center w-full">
        <img
          src="https://static1.squarespace.com/static/544e5e99e4b0b1199cf8d579/t/56589034e4b027c789a412e1/1662456295121/"
          alt="Jacob Meatpacker"
          class="mx-auto w-32"
        />
        <p class="text-lg italic mt-2">Authentic American Street Food</p>
      </div>

      <!-- Hamburger Button -->
      <button @click="toggleMenu" class="absolute top-4 right-4 z-50 md:hidden">
        <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round"
                d="M4 6h16M4 12h16M4 18h16"/>
        </svg>
      </button>
    </div>

    <!-- Mobile Menu -->
    <transition name="fade">
      <nav v-if="menuOpen" class="absolute top-0 left-0 w-full h-screen bg-[#121212] z-40 flex flex-col items-center justify-center space-y-6 text-xl">
        <a v-for="item in menuItems" :key="item.id" :href="`#${item.id}`" class="hover:underline" @click="toggleMenu">
          {{ item.label }}
        </a>
      </nav>
    </transition>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)

function toggleMenu() {
  menuOpen.value = !menuOpen.value
}

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
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.3s ease;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
</style>
