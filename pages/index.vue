<template>
  <div class="max-w-2xl mx-auto px-4 py-10">
    <Header />

    <AccordionSection
      title="Antipasti"
      :items="[
        { name: 'Burrata des Pouilles', price: 12, description: 'Crémeuse, servie avec tomates cerises confites & huile basilic' },
        { name: 'Carpaccio di Manzo', price: 14, description: 'Bœuf mariné, roquette, parmesan, câpres' }
      ]"
    />

    <AccordionSection
      title="Pizza Bianca"
      :items="[
        { name: '4 Formaggi', price: 17, description: 'Ricotta di bufala, mozza fior di latte, bleu, pecorino sarde' },
        { name: 'Tartufata', price: 22, description: 'Crème de truffe noire, roquette, parmigiano' }
      ]"
      :addons="[
        { name: 'Burrata', price: 3 },
        { name: 'Truffe râpée', price: 4 }
      ]"
    />

    <AccordionSection
      title="Pasta Fresca"
      :items="[
        { name: 'Carbonara', price: 16, description: 'Pancetta, œuf, pecorino, poivre noir' },
        { name: 'Pesto Genovese', price: 15, description: 'Basilic frais, pignons, parmesan' }
      ]"
      :addons="[
        { name: 'Jambon San Daniele', price: 3.5 },
        { name: 'Pâtes sans gluten', price: 2 }
      ]"
    />

    <AccordionSection
      title="Salades Gourmandes"
      :items="[
        { name: 'Rosetta Bowl', price: 14, description: 'Quinoa, avocat, tomate, pois chiche, citron vert' },
        { name: 'Salade Caprese', price: 13, description: 'Mozzarella di bufala, tomates anciennes, pesto maison' }
      ]"
    />

    <AccordionSection
      title="Viandes & Poissons"
      :items="[
        { name: 'Filet de bœuf grillé', price: 26, description: 'Purée de patate douce, jus réduit au vin rouge' },
        { name: 'Pavé de saumon rôti', price: 22, description: 'Légumes croquants, émulsion citronnée' }
      ]"
      :addons="[
        { name: 'Sauce au poivre', price: 2 },
        { name: 'Purée truffée', price: 3 }
      ]"
    />

    <AccordionSection
      title="Desserts Maison"
      :items="[
        { name: 'Tiramisu Classico', price: 8, description: 'Mascarpone, café, cacao, biscuit imbibé maison' },
        { name: 'Panna Cotta', price: 7, description: 'Vanille de Madagascar, coulis de framboise' }
      ]"
    />

    <Footer />
  </div>
</template>

<script setup>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'
import AccordionSection from '~/components/AccordionSection.vue'
</script>
