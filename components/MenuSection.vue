<template>
  <section class="my-8">
    <h2 class="text-2xl font-bold text-center text-orange-400 mb-6">{{ title }}</h2>
    <div class="space-y-4">
      <MenuItem
        v-for="(item, i) in items"
        :key="i"
        :item="item"
        :reverse="i % 2 !== 0"
      />
    </div>
  </section>
</template>

<script setup>
import MenuItem from './MenuItem.vue'
defineProps({ title: String, items: Array })
</script>
