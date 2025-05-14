<template>
  <div class="border-b border-[#e7e2dd] pb-4">
    <div class="flex justify-between items-start">
      <div>
        <h3 class="text-lg font-medium text-[#1b3b34]">{{ name }}</h3>
        <p class="text-sm text-[#555] italic">{{ description }}</p>
      </div>
      <span class="text-[#a16c4f] font-semibold whitespace-nowrap">{{ price }}</span>
    </div>
  </div>
</template>

<script setup>
defineProps(['name', 'price', 'description'])
</script>
