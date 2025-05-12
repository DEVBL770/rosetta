<template>
  <section class="my-8">
    <h2 class="text-3xl font-extrabold font-serif border-b-2 border-gray-300 pb-2 mb-4">{{ title }}</h2>
    <div class="grid gap-6">
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
  items: Array
});
</script>

<style scoped>
@media (max-width: 767px) {
  .menu-item p {
    white-space: normal; /* Permet à la description de se casser sur plusieurs lignes */
  }
}
</style>
