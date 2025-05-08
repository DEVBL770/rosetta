<template> 
  <div class="bg-[#121212] font-serif text-white">
    <Header />
    <main class="max-w-4xl mx-auto">
      <MenuSection
        id="burgers"
        title="Burgers"
        :items="burgers"
      />
      <MenuSection
        id="bagels"
        title="Bagels"
        :items="bagels"
      />
      <MenuSection
        id="sides"
        title="Accompagnements"
        :items="sides"
      />
      <MenuSection
        id="desserts"
        title="Desserts"
        :items="desserts"
      />
      <MenuSection
        id="boissons"
        title="Boissons"
        :items="boissons"
      />
    </main>
    <Footer />
  </div>
</template>

<script setup>
import Header from '~/components/Header.vue';
import Footer from '~/components/Footer.vue';
import MenuSection from '~/components/MenuSection.vue';

const burgers = [
  {
    name: 'Jacob',
    description: 'Double 100% Bœuf, fromage, oignons caramélisés, champignons, charcuterie fumée, tomate, cornichons, iceberg',
    price: 27.00
  },
  {
    name: 'Pepper Cheese',
    description: 'Sauce au poivre vert maison, 100% Bœuf, fromage, oignons caramélisés, tomate, cornichons, iceberg',
    price: 18.40
  },
];

const bagels = [
  {
    name: 'Dinde',
    description: 'Mayonnaise maison, dinde fumée, tomate, pickles',
    price: 8.90
  },
  {
    name: 'Pastrami',
    description: 'Mayonnaise maison, pastrami, tomate, pickles',
    price: 9.40
  },
];

const sides = [
  {
    name: 'Frites maison',
    description: 'Frites fraîches préparées sur place',
    price: 6.00
  },
  {
    name: 'Chicken Crunch',
    description: 'Poulet croustillant maison',
    price: 9.90
  },
];

const desserts = [
  {
    name: 'Tarte aux pommes maison',
    description: 'Tarte aux pommes faite maison',
    price: 6.00
  },
  {
    name: 'Mousse au chocolat maison',
    description: 'Mousse au chocolat faite maison',
    price: 6.00
  },
];

const boissons = [
  {
    name: 'Coca-Cola',
    description: '33 cL',
    price: 3.50
  },
  {
    name: 'Evian',
    description: '50 cL',
    price: 3.50
  },
];
</script>
