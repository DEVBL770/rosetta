<template>
  <section class="my-8 px-6">
    <h2 class="text-2xl title-font border-b-2 border-gray-400 inline-block mb-4 text-gray-900">{{ title }}</h2>
    <div>
      <MenuItem v-for="(item, index) in items" :key="index" :name="item.name" :description="item.description" :price="item.price" />
    </div>
  </section>
</template>

<script setup lang="ts">
import MenuItem from './MenuItem.vue'

defineProps({
  title: String,
  items: Array
})
</script>
