<template>
  <section :id="sectionId" class="pt-24 scroll-mt-24 px-4 sm:px-8 lg:px-16">
    <h2 class="text-3xl font-bold text-center text-gray-800 mb-6">{{ title }}</h2>
    <div class="grid gap-4 md:grid-cols-2 lg:grid-cols-3">
      <MenuItem
        v-for="(item, index) in items"
        :key="index"
        :name="item.name"
        :description="item.description"
        :price="item.price"
      />
    </div>
  </section>
</template>

<script setup>
defineProps({
  title: String,
  items: Array,
  sectionId: String
});
</script>
