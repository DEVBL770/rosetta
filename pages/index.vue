<template>
  <div class="bg-[#fdfaf4] min-h-screen text-gray-800">
    <Header />
    <main class="max-w-2xl mx-auto py-8">
      <MenuSection title="Entrées" :items="entrees" />
      <MenuSection title="Plats principaux" :items="plats" />
      <MenuSection title="Desserts" :items="desserts" />
    </main>
    <Footer />
  </div>
</template>

<script setup lang="ts">
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import MenuSection from '@/components/MenuSection.vue'

const entrees = [
  { name: 'Bruschetta', description: 'Tomates cerises, ail, basilic frais', price: 8 },
  { name: 'Carpaccio de bœuf', description: 'Roquette, parmesan', price: 12 }
]

const plats = [
  { name: 'Spaghetti Carbonara', description: 'Pancetta, œuf, pecorino', price: 15 },
  { name: 'Risotto aux champignons', description: 'Crème de truffe', price: 17 }
]

const desserts = [
  { name: 'Tiramisu', description: 'Classique italien, mascarpone', price: 7 },
  { name: 'Panna Cotta', description: 'Coulis de fruits rouges', price: 6 }
]
</script>
