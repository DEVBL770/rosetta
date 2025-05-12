<template>
  <div class="w-full max-w-3xl mx-auto px-4 py-8">
    <div v-for="(section, index) in sections" :key="index" class="mb-4">
      <!-- Button d'accordéon avec prix en haut à droite -->
      <button
        @click="toggle(index)"
        class="w-full flex justify-between items-center bg-gray-800 text-white px-4 py-3 text-xl font-semibold rounded shadow"
      >
        <span>{{ section.title }}</span>
        <span>{{ activeIndex === index ? '-' : '+' }}</span>
      </button>

      <!-- Transition pour l'animation -->
      <transition name="fade">
        <div v-show="activeIndex === index" class="mt-2 px-4 py-2 bg-gray-900 rounded">
          <ul class="space-y-4">
            <li
              v-for="(item, i) in section.items"
              :key="i"
              class="flex justify-between border-b border-gray-700 pb-2"
            >
              <div>
                <p class="font-bold text-white">{{ item.name }}</p>
                <p class="text-sm text-gray-400">{{ item.description }}</p>
              </div>
              <p class="text-white font-semibold">{{ item.price.toFixed(2) }} €</p>
            </li>
          </ul>
        </div>
      </transition>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const activeIndex = ref(null)

function toggle(index) {
  activeIndex.value = activeIndex.value === index ? null : index
}

const sections = [
  {
    title: 'Meat Burgers',
    items: [
      { name: 'Classic', description: 'Mayonnaise maison, 100 % Bœuf, oignons caramélisés maison, tomate, cornichons aigre doux, iceberg.', price: 15.50 },
      { name: 'Cheese', description: 'Mayonnaise maison, 100 % Bœuf, fromage (parve), oignons caramélisés maison, tomate, cornichons aigre doux, iceberg.', price: 16.50 },
      { name: 'Pepper', description: 'Sauce au Poivre Vert maison, 100 % Bœuf, oignons caramélisés maison, tomate, cornichons aigre doux, iceberg', price: 16.50 },
      { name: 'Deli', description: 'Mayonnaise maison, 100 % Bœuf, oignons caramélisés, «Deli» charcuterie fumée et snackée, tomate, cornichons aigre doux, iceberg', price: 17.50 },
      { name: 'Mushroom', description: 'Mayonnaise maison, 100 % Bœuf, champignons poêlés au vin blanc, cornichons aigre doux, iceberg', price: 16.50 },
      { name: 'Peno', description: 'Mayonnaise maison, 100% Boeuf, oignons caramélisés, piments snackés au miel, tomate, cornichons aigre doux, iceberg', price: 16.50 },
      { name: 'Deli Cheese', description: 'Mayonnaise maison, 100% Boeuf, fromage (parve), oignons caramélisés maison, "Deli" charcuterie fumée et snackée, tomate, cornichons aigre doux, iceberg', price: 18.40 },
      { name: 'Pepper Cheese', description: 'Sauce au Poivre Vert maison, 100% Boeuf, fromage (parve), oignons caramélisés maison, tomate, cornichons aigre doux, iceberg', price: 18.40 },
      { name: 'Mushroom Cheese', description: 'Mayonnaise maison, 100% Boeuf, fromage (parve), champignons poêlés au vin blanc, tomate, cornichons aigre doux, iceberg', price: 17.90 },
      { name: 'Delipeno', description: 'Mayonnaise maison, 100% Boeuf, oignons caramélisés, "Deli" charcuterie fumée et snackée, piments snackés au miel, tomate, cornichons aigre doux, iceberg', price: 18.40 },
      { name: 'Pepper Deli', description: 'Sauce au Poivre Vert maison, 100% Boeuf, oignons caramélisés maison, "Deli" charcuterie fumée et snackée, tomate, cornichons aigre doux, iceberg', price: 18.40 },
      { name: 'Jacob', description: 'Sauce au Poivre Vert maison, DOUBLE 100% Boeuf, fromage (parve), oignons caramélisés maison, champignons poêlés au vin blanc, "Deli" charcuterie fumée et snackée, tomate, cornichons, aigre doux, iceberg', price: 27.00 },
    ],
  },
  {
    title: 'Chicken Burgers',
    items: [
      { name: 'Fried Chicken', description: 'Moutarde au miel, poitrine de poulet « Panée maison », oignons frits, tomate, iceberg', price: 16.90 },
      { name: 'P.C.C.', description: 'Sauce au Poivre Vert maison, poitrine de poulet "Panée maison", fromage (parve), oignons caramélisés maison, iceberg', price: 17.50 },
      { name: 'Caesar', description: 'Sauce Caesar maison, poitrine de poulet "Panée maison", fromage (parve), tomate, iceberg', price: 16.90 },
      { name: 'Crunch Burger', description: '4 sauces (pepper, caesar, sweet chili, moutarde miel), avocat, Chicken crunch maison, roquette, citron', price: 17.90 },
      { name: 'Grilled Chicken', description: 'Sweet and Sour sauce, poitrine de poulet grillée, tomate, iceberg', price: 16.90 },
    ],
  },
  {
    title: 'Fish Burgers',
    items: [
      { name: 'Cabillaud', description: 'Sauce Tartare maison, Cabillaud Pané maison, fromage (parve)', price: 22.00 },
    ],
  },
  {
    title: 'Burgers Signature',
    items: [
      { name: 'Pulled Beef', description: 'Mayonnaise à l\'ail, boeuf effiloché et caramélisé, chou rouge, estragon & noisettes torrefiées', price: 22.00 },
      { name: 'Motz', description: 'Mayonnaise maison, double viande fine "smashée", double cheese (parve), oignons, cornichons', price: 18.40 },
    ],
  },
  {
    title: 'Basic Sides',
    items: [
      { name: 'Frites Maison', description: '', price: 5.50 },
    ],
  },
  {
    title: 'Appetizers Sides',
    items: [
      { name: 'Chicken Crunch X6', description: '', price: 9.90 },
      { name: 'Chicken Crunch X9', description: '', price: 14.50 },
      { name: 'Chicken Crunch X12', description: '', price: 18.50 },
      { name: 'Onion Rings Maison X6', description: '', price: 8.00 },
      { name: 'Onion Rings Maison X9', description: '', price: 11.00 },
      { name: 'Onion Rings Maison X12', description: '', price: 13.50 },
      { name: 'Fish Sticks X6', description: '', price: 12.00 },
      { name: 'Fish Sticks X9', description: '', price: 18.00 },
      { name: 'Fish Sticks X12', description: '', price: 24.00 },
    ],
  },
  {
    title: 'Desserts',
    items: [
      { name: 'Salade de fruits frais', description: '', price: 5.50 },
      { name: 'Mousse au chocolat Maison', description: '', price: 5.50 },
    ],
  },
  {
    title: 'Boissons',
    items: [
      { name: 'Coca-Cola', description: '330ml', price: 3.00 },
      { name: 'Coca-Cola Light', description: '330ml', price: 3.00 },
      { name: 'Coca-Cola Zero', description: '330ml', price: 3.00 },
      { name: 'Sprite', description: '330ml', price: 3.00 },
      { name: 'Ice Tea Pêche', description: '330ml', price: 3.00 },
      { name: 'Ice Tea Citron Vert', description: '330ml', price: 3.00 },
      { name: 'Evian', description: '500ml', price: 3.00 },
      { name: 'Badoit', description: '330ml', price: 3.00 },
      { name: 'Orangina', description: '330ml', price: 3.00 },
      { name: 'Dr Pepper', description: '330ml', price: 3.50 },
      { name: 'San Pellegrino Orange', description: '330ml', price: 3.50 },
      { name: 'San Pellegrino Pamplemousse', description: '330ml', price: 3.50 },
      { name: 'Boylan Cane Cola', description: '355ml', price: 4.90 },
      { name: 'Heineken', description: '330ml', price: 4.50 },
      { name: 'Carlsberg', description: '330ml', price: 6.00 },
      { name: 'Brooklyn Beer Brown', description: '355ml', price: 8.00 },
      { name: 'Brooklyn Beer Summer', description: '355ml', price: 8.00 },
      { name: 'Brooklyn Beer 1/2 Ale', description: '355ml', price: 8.00 },
    ],
  },
]
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: all 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: scaleY(0.95);
}

button span:last-child {
  font-size: 1.2em;
}
</style>
