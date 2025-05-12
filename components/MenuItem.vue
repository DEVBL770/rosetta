<template>
  <div class="flex justify-between items-start py-4 border-b border-gray-600">
    <div class="w-3/4 pr-4">
      <h3 class="text-lg font-semibold">{{ name }}</h3>
      <p class="text-sm text-white-700 break-words">{{ description }}</p>
    </div>
    <div class="w-1/4 text-right">
      <span class="text-md font-bold text-white-800">{{ price }} €</span>
    </div>
  </div>
</template>

<script setup>
defineProps({
  name: String,
  description: String,
  price: [String, Number]
});
</script>
