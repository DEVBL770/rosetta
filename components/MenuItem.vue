<template>
  <div class="border-b border-[#e7e2dd] pb-4">
    <div class="flex justify-between items-start">
      <div>
        <h3 class="text-lg font-medium text-[#18534f]">{{ name }}</h3>
        <p class="text-sm text-[#555] italic">{{ description }}</p>
      </div>
      <span class="text-[#cc9fbb] font-semibold whitespace-nowrap">{{ price }}</span>
    </div>
  </div>
</template>

<script setup>
defineProps(['name', 'price', 'description'])
</script>
