<template>
  <div class="flex flex-col sm:flex-row gap-4 items-center bg-white/80 rounded-xl p-4 shadow hover:scale-[1.01] transition">
    <img :src="item.image" alt="" class="w-full sm:w-36 h-36 object-cover rounded-lg">
    <div class="flex-1 text-center sm:text-left">
      <h3 class="text-xl font-bold text-rose-500">{{ item.name }}</h3>
      <p class="text-sm text-gray-700">{{ item.description }}</p>
    </div>
    <div class="text-orange-500 font-semibold text-lg">{{ item.price }} €</div>
  </div>
</template>

<script setup>
defineProps({ item: Object })
</script>
