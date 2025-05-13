<template>
  <div class="bg-white border border-gray-200 rounded-xl p-4 shadow-sm hover:shadow-md transition">
    <h3 class="text-xl font-semibold mb-2">{{ name }}</h3>
    <p class="text-gray-600 mb-2">{{ description }}</p>
    <p class="text-primary font-bold text-lg">{{ price }} €</p>
  </div>
</template>

<script setup>
defineProps({
  name: String,
  description: String,
  price: Number
})
</script>
