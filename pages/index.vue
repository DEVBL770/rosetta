<template>
  <div class="bg-white text-gray-800">
    <Header />

    <!-- Hero Section -->
    <section class="text-center py-20 px-4">
      <h1 class="text-4xl font-bold mb-4">Bienvenue chez Jacob Meat Peaker</h1>
      <p class="text-lg text-gray-600 max-w-xl mx-auto">Explorez notre menu de viandes grillées, burgers, poissons et plus encore, dans un cadre digne des meilleures tables parisiennes.</p>
    </section>

    <!-- Menu Sections -->
    <MenuSection
      section-id="burgers"
      title="Nos Burgers"
      :items="burgers"
    />
    <MenuSection
      section-id="chicken"
      title="Poulet"
      :items="chicken"
    />
    <MenuSection
      section-id="fish"
      title="Poisson"
      :items="fish"
    />

    <Footer />
  </div>
</template>

<script setup>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'
import MenuSection from '~/components/MenuSection.vue'

const burgers = [
  { name: 'Classic Burger', description: 'Steak, fromage, salade, tomate', price: '12€' },
  { name: 'Cheeseburger', description: 'Double cheddar, oignons caramélisés', price: '13€' },
]

const chicken = [
  { name: 'Poulet rôti', description: 'Mariné aux herbes de Provence', price: '14€' },
  { name: 'Wings épicées', description: 'Sauce maison', price: '9€' },
]

const fish = [
  { name: 'Filet de saumon', description: 'Grillé à la perfection', price: '15€' },
  { name: 'Fish & Chips', description: 'Avec sauce tartare', price: '13€' },
]
</script>
