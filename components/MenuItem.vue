<template>
  <div class="flex flex-col sm:flex-row justify-between items-start py-4 border-b border-gray-600">
    <div class="flex-1">
      <h3 class="text-lg font-semibold">{{ name }}</h3>
      <p class="text-sm text-white-700">{{ description }}</p>
    </div>
    <span class="text-md font-bold text-white-800 mt-2 sm:mt-0 sm:text-right">{{ price }} €</span>
  </div>
</template>

<script setup>
defineProps({
  name: String,
  description: String,
  price: String
});
</script>

<style scoped>
/* Assurer le retour à la ligne dans la description sur mobile */
@media (max-width: 767px) {
  .menu-item p {
    white-space: normal; /* Permet à la description de se casser sur plusieurs lignes */
  }
}
</style>
