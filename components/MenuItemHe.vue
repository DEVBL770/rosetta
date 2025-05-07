<template>
    <div class="flex justify-between border-b border-dashed border-gray-300 py-2 direction-rtl">
      <!-- Prix à gauche -->
      <span class="price-font text-gray-700">₪{{ price }}</span>
  
      <!-- Texte à droite -->
      <div class="text-right">
        <h3 class="text-lg title-font text-gray-800">{{ name }}</h3>
        <p class="text-sm text-gray-500 italic">{{ description }}</p>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  defineProps({
    name: String,
    description: String,
    price: Number
  })
  </script>
  