<template>
 <div class="bg-[#121212] font-black-paris text-white">
    <Header />
    <main class="max-w-4xl mx-auto px-4 py-8 space-y-16">
      <MenuSection id="burgers" title="Burgers" :items="burgers" />
      <MenuSection id="chicken" title="Chicken" :items="chicken" />
      <MenuSection id="fish" title="Fish" :items="fish" />
      <MenuSection id="signatures" title="Signatures" :items="signatures" />
      <MenuSection id="bagels" title="Bagels" :items="bagels" />
      <MenuSection id="sandwichs" title="Sandwichs" :items="sandwichs" />
      <MenuSection id="sides" title="Accompagnements" :items="sides" />
      <MenuSection id="desserts" title="Desserts" :items="desserts" />
      <MenuSection id="boissons" title="Boissons" :items="boissons" />
    </main>
    <Footer />
  </div>
</template>

<script setup>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'
import MenuSection from '~/components/MenuSection.vue'

// Menu complet Jacob Meatpacker
const burgers = [
  {
    name: 'Jacob',
    description: 'Double 100% Bœuf, fromage, oignons caramélisés, champignons, charcuterie fumée, tomate, cornichons, iceberg',
    price: 27.00,
  },
  {
    name: 'Pepper Cheese',
    description: 'Sauce au poivre vert maison, 100% Bœuf, fromage, oignons caramélisés, tomate, cornichons, iceberg',
    price: 18.40,
  },
  {
    name: 'Cheese Burger',
    description: '100% Bœuf, fromage, oignons caramélisés, tomate, cornichons, iceberg',
    price: 17.00,
  },
  {
    name: 'Hamburger',
    description: '100% Bœuf, oignons caramélisés, tomate, cornichons, iceberg',
    price: 15.00,
  },
]

const chicken = [
  {
    name: 'Crunchy',
    description: 'Poulet croustillant, fromage, oignons caramélisés, tomate, cornichons, iceberg, sauce blanche maison',
    price: 17.00,
  },
  {
    name: 'Chicken Classic',
    description: 'Blanc de poulet grillé, fromage, oignons caramélisés, tomate, cornichons, iceberg, sauce blanche maison',
    price: 17.00,
  },
]

const fish = [
  {
    name: 'Fish Burger',
    description: 'Filet de poisson pané, sauce tartare, iceberg, tomate, oignon rouge',
    price: 15.00,
  },
]

const signatures = [
  {
    name: 'Giant Pastrami',
    description: 'Pastrami maison, sauce moutarde douce, pickles, tomate, iceberg',
    price: 17.50,
  },
  {
    name: 'Smoked Turkey',
    description: 'Dinde fumée, sauce moutarde douce, pickles, tomate, iceberg',
    price: 17.00,
  },
  {
    name: 'Chicken Pastrami',
    description: 'Poulet grillé, pastrami, sauce moutarde douce, pickles, tomate, iceberg',
    price: 17.50,
  },
]

const bagels = [
  {
    name: 'Bagel Dinde',
    description: 'Dinde fumée, sauce mayonnaise maison, pickles, tomate, iceberg',
    price: 8.90,
  },
  {
    name: 'Bagel Pastrami',
    description: 'Pastrami, sauce mayonnaise maison, pickles, tomate, iceberg',
    price: 9.40,
  },
]

const sandwichs = [
  {
    name: 'Pastrami',
    description: 'Pastrami maison, moutarde douce, pickles, pain baguette',
    price: 13.50,
  },
  {
    name: 'Dinde',
    description: 'Dinde fumée, moutarde douce, pickles, pain baguette',
    price: 13.00,
  },
]

const sides = [
  {
    name: 'Frites maison',
    description: 'Frites fraîches préparées sur place',
    price: 6.00,
  },
  {
    name: 'Chicken Crunch',
    description: 'Poulet croustillant maison',
    price: 9.90,
  },
  {
    name: 'Onion Rings',
    description: 'Rondelles d’oignon panées croustillantes',
    price: 7.00,
  },
  {
    name: 'Coleslaw',
    description: 'Salade de chou maison',
    price: 5.00,
  },
]

const desserts = [
  {
    name: 'Tarte aux pommes maison',
    description: 'Tarte faite maison',
    price: 6.00,
  },
  {
    name: 'Mousse au chocolat maison',
    description: 'Mousse faite maison',
    price: 6.00,
  },
  {
    name: 'Crème dessert vanille',
    description: 'Crème onctueuse à la vanille',
    price: 4.50,
  },
]

const boissons = [
  {
    name: 'Coca-Cola',
    description: '33 cl',
    price: 3.50,
  },
  {
    name: 'Coca-Cola Zero',
    description: '33 cl',
    price: 3.50,
  },
  {
    name: 'Fanta',
    description: '33 cl',
    price: 3.50,
  },
  {
    name: 'Sprite',
    description: '33 cl',
    price: 3.50,
  },
  {
    name: 'Eau Evian',
    description: '50 cl',
    price: 3.50,
  },
]
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&display=swap');

.font-black-paris {
  font-family: 'Playfair Display', serif;
}
</style>
