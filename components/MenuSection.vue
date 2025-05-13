<template>
  <section :id="sectionId" class="py-12 px-4">
    <h2 class="text-3xl font-bold text-center mb-8">{{ title }}{{ description }}</h2>
    <div class="space-y-6">
      <div v-for="(item, index) in items" :key="index" class="flex justify-between items-center p-4 border-b border-gray-200">
        <div class="flex-1">
          <h3 class="text-xl font-semibold">{{ item.name }}</h3>
          <p class="text-gray-600">{{ item.description }}</p>
        </div>
        <div class="w-24 text-right">
          <span class="text-lg font-bold">{{ item.price }} €</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
defineProps({
  sectionId: String,
  title: String,
  items: Array
})
</script>

<style scoped>
/* Centrer le texte et ajuster l'apparence du prix */
.w-24 {
  width: 6rem; /* Ajuster la taille du container du prix */
}
.text-right {
  text-align: right;
}
</style>
