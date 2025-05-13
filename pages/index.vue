<template>
  <div class="bg-white text-gray-800">
    <Header />

    <!-- Hero Section -->
    <section class="text-center py-5 px-2">
      <h1 class="text-4xl font-bold mb-4">Bienvenue chez Jacob Meat Peaker</h1>
      <p class="text-lg text-gray-600 max-w-l mx-auto">Véritable ambassade de la street food américaine, Jacob Meatpacker est né de la volonté du créateur de faire partager son amour des produits "Maison"</p>
    </section>

    <div class="my-8">
      <hr class="border-t-1 border-gray-300 mx-auto w-1/4 opacity-70" />
    </div>

    <!-- Menu Sections -->
    <MenuSection
      section-id="burgers"
      title="Meat Burgers"
      description="Tous nos burgers sont préparés avec de la viande 100% Bœuf, du pain fait maison et des sauces maison."
      :items="burgers"
    />
    <MenuSection
      section-id="chicken"
      title="Chicken"
      :items="chicken"
    />
    <MenuSection
      section-id="fish"
      title="Fish"
      :items="fish"
    />
    <MenuSection
      section-id="signatures"
      title="Signatures"
      :items="signatures"
    />
    <MenuSection
      section-id="sides"
      title="Sides"
      :items="sides"
    />
    <MenuSection
      section-id="desserts"
      title="Desserts"
      :items="desserts"
    />
    <MenuSection
      section-id="boissons"
      title="Drinks"
      :items="boissons"
    />

    <Footer />
  </div>
</template>

<script setup>
import { onMounted } from 'vue'
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'
import MenuSection from '~/components/MenuSection.vue'

// Ajout de la correction du scroll
onMounted(() => {
  window.scrollTo(0, 0); // Cette ligne permet de revenir en haut de la page
})

// BURGERS
const burgers = [
  { name: 'Classic', description: 'Mayonnaise maison, 100 % Bœuf, oignons caramélisés maison, tomate, cornichons aigre doux, iceberg', price: 15.50 },
  { name: 'Cheese', description: 'Mayonnaise maison, 100 % Bœuf, fromage (parve), oignons caramélisés maison, tomate, cornichons aigre doux, iceberg', price: 16.50 },
  { name: 'Pepper', description: 'Sauce au Poivre Vert maison, 100 % Bœuf, oignons caramélisés maison, tomate, cornichons aigre doux, iceberg', price: 16.50 },
  { name: 'Deli', description: 'Mayonnaise maison, 100 % Bœuf, oignons caramélisés, «Deli» charcuterie fumée et snackée, tomate, cornichons aigre doux, iceberg', price: 17.50 },
  { name: 'Mushroom', description: 'Mayonnaise maison, 100 % Bœuf, champignons poêlés au vin blanc, cornichons aigre doux, iceberg', price: 16.50 },
  { name: 'Peno', description: 'Mayonnaise maison, 100% Boeuf, oignons caramélisés, piments snackés au miel, tomate, cornichons aigre doux, iceberg', price: 16.50 },
  { name: 'Deli Cheese', description: 'Mayonnaise maison, 100% Boeuf, fromage (parve), oignons caramélisés maison, "Deli" charcuterie fumée et snackée, tomate, cornichons aigre doux, iceberg', price: 18.40 },
  { name: 'Pepper Cheese', description: 'Sauce au Poivre Vert maison, 100% Boeuf, fromage (parve), oignons caramélisés maison, tomate, cornichons aigre doux, iceberg', price: 18.40 },
  { name: 'Mushroom Cheese', description: 'Mayonnaise maison, 100% Boeuf, fromage (parve), champignons poêlés au vin blanc, tomate, cornichons aigre doux, iceberg', price: 17.90 },
  { name: 'Delipeno', description: 'Mayonnaise maison, 100% Boeuf, oignons caramélisés, "Deli" charcuterie fumée et snackée, piments snackés au miel, tomate, cornichons aigre doux, iceberg', price: 18.40 },
  { name: 'Pepper Deli', description: 'Sauce au Poivre Vert maison, 100% Boeuf, oignons caramélisés maison, "Deli" charcuterie fumée et snackée, tomate, cornichons aigre doux, iceberg', price: 18.40 },
  { name: 'Jacob', description: 'Sauce au Poivre Vert maison, DOUBLE 100% Boeuf, fromage (parve), oignons caramélisés maison, champignons poêlés au vin blanc, "Deli" charcuterie fumée et snackée, tomate, cornichons aigre doux, iceberg', price: 27.00 }
]

// CHICKEN
const chicken = [
  { name: 'Fried Chicken', description: 'Moutarde au miel, poitrine de poulet « Panée maison », oignons frits, tomate, iceberg', price: 16.90 },
  { name: 'P.C.C.', description: 'Sauce au Poivre Vert maison, poitrine de poulet "Panée maison", fromage (parve), oignons caramélisés maison, iceberg', price: 17.50 },
  { name: 'Caesar', description: 'Sauce Caesar maison, poitrine de poulet "Panée maison", fromage (parve), tomate, iceberg', price: 16.90 },
  { name: 'Crunch Burger', description: '4 sauces (pepper, caesar, sweet chili, moutarde miel), avocat, Chicken crunch maison, roquette, citron', price: 17.90 },
  { name: 'Grilled Chicken', description: 'Sweet and Sour sauce, poitrine de poulet grillée, tomate, iceberg', price: 16.90 }
]

// FISH
const fish = [
  { name: 'Cabillaud', description: 'Sauce Tartare maison, Cabillaud Pané maison, fromage (parve)', price: 22.00 }
]

// SIGNATURES
const signatures = [
  { name: 'Pulled Beef', description: 'Mayonnaise à l\'ail, boeuf effiloché et caramélisé, chou rouge, estragon & noisettes torrefiées', price: 22.00 },
  { name: 'Motz', description: 'Mayonnaise maison, double viande fine "smashée", double cheese (parve), oignons, cornichons', price: 18.40 }
]

// SIDES
const sides = [
  { name: 'Frites Maison', description: '', price: 5.50 },
  { name: 'Chicken Crunch X6', description: '', price: 9.90 },
  { name: 'Chicken Crunch X9', description: '', price: 14.50 },
  { name: 'Chicken Crunch X12', description: '', price: 18.50 },
  { name: 'Onion Rings Maison X6', description: '', price: 8.00 },
  { name: 'Onion Rings Maison X9', description: '', price: 11.00 },
  { name: 'Onion Rings Maison X12', description: '', price: 13.50 },
  { name: 'Fish Sticks X6', description: '', price: 12.00 },
  { name: 'Fish Sticks X9', description: '', price: 18.00 },
  { name: 'Fish Sticks X12', description: '', price: 24.00 }
]

// DESSERTS
const desserts = [
  { name: 'Salade de fruits frais', description: '', price: 5.50 },
  { name: 'Mousse au chocolat Maison', description: '', price: 5.50 }
]

// BOISSONS
const boissons = [
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
  { name: 'Brooklyn Lager', description: '355ml', price: 8.00 }
]
</script>

