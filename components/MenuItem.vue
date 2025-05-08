<template>
  <div class="flex justify-between items-start">
    <div>
      <h3 class="text-lg font-semibold">{{ name }}</h3>
      <p class="text-sm text-white-700">{{ description }}</p>
    </div>
    <span class="text-md font-bold text-white-800">{{ price }} €</span>
  </div>
</template>

<script setup>
defineProps({
  name: String,
  description: String,
  price: String
});
</script>
